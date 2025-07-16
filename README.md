Smart Medication Assistant: Your AI-Powered Health Companion
Unleash the power of intelligent healthcare with the Smart Medication Assistant! This innovative web application is meticulously crafted to revolutionize how patients manage their medications and connect with their doctors. Experience a future where adherence is effortless and communication is seamless, all powered by cutting-edge AI.

✨ Key Features
Intelligent Patient Medication Management: 💊

Effortlessly add and track medications with precise dosages, times, and personalized instructions.

Digitally archive past medications and access a comprehensive historical record.

Activate smart reminders for medication times, ensuring no dose is missed (experimental feature).

Gain clarity with AI-powered medication explanations (Gemini AI), transforming complex medical jargon into easy-to-understand insights.

Doctor's Intuitive Dashboard: 🧑‍⚕️

Access a streamlined list of all linked patients.

Initiate secure linking requests to patients using their unique sharing code (UID).

Directly add and modify medications for their patients with precision.

Monitor vital patient and prescribed medication statistics through insightful analytics.

Seamless & Secure Communication: 💬

Engage in real-time chat with patients, fostering immediate support and guidance.

Securely attach and share essential files within chat conversations.

Prioritize urgent patient needs with categorized messages (normal, urgent, emergency) for prompt alerts.

Advanced Account Management: ⚙️

Streamlined login and registration for both patients and doctors with distinct roles.

Effortless password reset functionality.

Personalized profile updates (name, age, health conditions, specialty).

Enhanced security with simulated Two-Factor Authentication (2FA) using QR codes.

Empower patients to provide valuable feedback through doctor ratings.

Adaptive & Elegant Design: 📱💻

Enjoy a fluid and responsive experience across all devices (mobile, tablet, desktop).

Personalize your interface with a comfortable Dark Mode toggle.

🚀 Technologies Used
Frontend:

HTML5

Tailwind CSS (for rapid and responsive design)

JavaScript (application logic)

Chart.js (for charts and statistics)

jsPDF (for exporting documents, available but not explicitly used currently)

QR Code Generator (for generating QR codes for 2FA)

jsQR (for reading QR codes, available but not explicitly used currently)

DOMPurify (for sanitizing user-generated content)

Backend & Database:

Firebase Authentication: For user registration and login management.

Cloud Firestore: Real-time NoSQL database for storing user data, medications, linking requests, and chats.

Firebase Storage: For storing attached files in chats.

Artificial Intelligence (AI):

Google Gemini API: For explaining medication information to patients (via a secure backend).

🛠️ Setup and Local Run
To run this application locally, follow these steps:

Clone the repository:

git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git
cd YOUR_REPOSITORY_NAME

(Replace YOUR_USERNAME and YOUR_REPOSITORY_NAME with your repository details).

Firebase Setup:

Go to Firebase Console and create a new project.

Add a web app to your project.

Copy the firebaseConfig provided by Firebase (includes apiKey, authDomain, projectId, storageBucket, messagingSenderId, appId).

Open endex.html and find the firebaseConfig object. Update the values with your project's values from the Firebase Console.

const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_AUTH_DOMAIN",
    projectId: "YOUR_PROJECT_ID",
    storageBucket: "YOUR_STORAGE_BUCKET",
    messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
    appId: "YOUR_APP_ID"
};

Firestore Rules:

In Firebase Console, navigate to Firestore Database -> Rules.

Ensure you have security rules that allow read and write access for authenticated users.

rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /artifacts/{appId}/users/{userId}/{documents=**} {
      allow read, write: if request.auth != null && request.auth.uid == userId;
    }
    match /artifacts/{appId}/public/data/{documents=**} {
      allow read, write: if request.auth != null;
    }
  }
}

Indexes: If you encounter query errors (especially those combining where and orderBy), you will need to create custom indexes. The Firebase Console will provide direct links to create these indexes. You can also update the firestore.indexes.json file and deploy it using the Firebase CLI.

Firebase Storage Rules (for chat file uploads):

In Firebase Console, navigate to Storage -> Rules.

Ensure you have a rule that allows authenticated users to upload and read files in the chat_files path:

rules_version = '2';
service firebase.storage {
  match /b/{bucket}/o {
    match /chat_files/{chatId}/{fileName} {
      allow read, write: if request.auth != null;
    }
  }
}

Setup CORS for Firebase Storage:

To allow file uploads from your local server, you will need to configure CORS on your storage bucket.

Ensure your cors.json file is in your project folder.

Use the Google Cloud SDK to apply the CORS settings to your storage bucket (replace YOUR_STORAGE_BUCKET_NAME with your bucket name from firebaseConfig):

gsutil cors set cors.json gs://YOUR_STORAGE_BUCKET_NAME

Setup Gemini API Key (Backend):

Important Security Note: In a production environment, you should never expose your Gemini API key directly in client-side code. It must be securely stored on a server-side backend (e.g., Firebase Cloud Functions) and all Gemini API calls should be proxied through this backend.

For local development, you can obtain a Gemini API key from Google AI Studio.

You will need to set up a backend (e.g., a Firebase Cloud Function) that receives requests from your frontend, makes the Gemini API call using the securely stored key, and returns the result. Update the backendEndpoint variable in endex.html with the URL of your deployed backend function.

const backendEndpoint = 'YOUR_FIREBASE_CLOUD_FUNCTION_URL/explainMedication'; // Replace with your cloud function URL

Run the Application:

endex.html cannot be run directly in the browser due to browser security restrictions (CORS) when accessing Firebase and Gemini API.

Recommended Option: Use the "Live Server" extension in Visual Studio Code. Open your project folder in VS Code, then right-click on endex.html and select "Open with Live Server".

Alternative (Simple Python Server): In your terminal within the project folder, you can run a simple web server:

python -m http.server 5500
# or
python3 -m http.server 5500

Then open your browser and navigate to http://localhost:5500/endex.html.

🤝 Contributing
We welcome contributions! If you have suggestions or improvements, feel free to open an issue or submit a pull request.

📄 License
This project is licensed under the MIT License. See the LICENSE file for more details.

مساعدك الدوائي الذكي: رفيقك الصحي المدعوم بالذكاء الاصطناعي
أطلق العنان لقوة الرعاية الصحية الذكية مع مساعدك الدوائي الذكي! هذا التطبيق المبتكر مصمم بعناية فائقة لإحداث ثورة في كيفية إدارة المرضى لأدويتهم والتواصل مع أطبائهم. اختبر مستقبلًا يصبح فيه الالتزام بالعلاج سهلاً والتواصل سلساً، كل ذلك بفضل قوة الذكاء الاصطناعي المتطورة.

✨ الميزات الرئيسية
إدارة الأدوية الذكية للمرضى: 💊

أضف وتتبع الأدوية بسهولة مع الجرعات الدقيقة، المواعيد، والتعليمات الشخصية.

أرشفة الأدوية القديمة رقميًا والوصول إلى سجل تاريخي شامل.

تفعيل التنبيهات الذكية لمواعيد الدواء، لضمان عدم تفويت أي جرعة (ميزة تجريبية).

احصل على وضوح تام مع شرح الأدوية المدعوم بالذكاء الاصطناعي (Gemini AI)، لتحويل المصطلحات الطبية المعقدة إلى رؤى سهلة الفهم.

لوحة تحكم الطبيب البديهية: 🧑‍⚕️

الوصول إلى قائمة مبسطة بجميع المرضى المرتبطين.

بدء طلبات ربط آمنة للمرضى باستخدام رمز المشاركة الفريد الخاص بهم (UID).

إضافة وتعديل الأدوية لمرضاهم مباشرةً وبدقة.

مراقبة إحصائيات المرضى والأدوية الموصوفة الهامة من خلال تحليلات ثاقبة.

تواصل سلس وآمن: 💬

إجراء محادثات فورية في الوقت الفعلي مع المرضى، لتقديم الدعم والإرشاد الفوري.

إرفاق ومشاركة الملفات الأساسية بشكل آمن ضمن محادثات الدردشة.

تحديد أولويات احتياجات المرضى العاجلة برسائل مصنفة (عادية، عاجلة، طارئة) للتنبيهات الفورية.

إدارة حساب متقدمة: ⚙️

تسجيل دخول وتسجيل مبسط لكل من المرضى والأطباء بأدوار منفصلة.

وظيفة إعادة تعيين كلمة المرور بسهولة.

تحديثات الملف الشخصي المخصصة (الاسم، العمر، الحالات الصحية، التخصص).

أمان معزز مع المصادقة الثنائية (2FA) المحاكية باستخدام رموز QR.

تمكين المرضى من تقديم ملاحظات قيمة من خلال تقييم الأطباء.

تصميم متكيف وأنيق: 📱💻

استمتع بتجربة سلسة ومتجاوبة عبر جميع الأجهزة (الجوال، التابلت، سطح المكتب).

خصص واجهتك مع خيار الوضع الداكن المريح.

🚀 التقنيات المستخدمة
الواجهة الأمامية (Frontend):

HTML5

Tailwind CSS (للتصميم السريع والمتجاوب)

JavaScript (منطق التطبيق)

Chart.js (للرسوم البيانية والإحصائيات)

jsPDF (لتصدير المستندات، متاح ولكن غير مستخدم حالياً بشكل صريح)

QR Code Generator (لتوليد رموز QR للمصادقة الثنائية)

jsQR (لقراءة رموز QR، متاح ولكن غير مستخدم حالياً بشكل صريح)

DOMPurify (لتنقية المحتوى الذي ينشئه المستخدم)

الواجهة الخلفية (Backend) وقاعدة البيانات:

Firebase Authentication: لإدارة تسجيل المستخدمين وتسجيل الدخول.

Cloud Firestore: قاعدة بيانات NoSQL في الوقت الفعلي لتخزين بيانات المستخدمين، الأدوية، طلبات الربط، والدردشات.

Firebase Storage: لتخزين الملفات المرفقة في الدردشات.

الذكاء الاصطناعي (AI):

Google Gemini API: لشرح معلومات الأدوية للمرضى (عبر واجهة خلفية آمنة).

🛠️ الإعداد والتشغيل المحلي
لتشغيل هذا التطبيق محليًا، اتبع الخطوات التالية:

استنساخ المستودع (Clone the repository):

git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git
cd YOUR_REPOSITORY_NAME

(استبدل YOUR_USERNAME و YOUR_REPOSITORY_NAME بتفاصيل مستودعك).

إعداد Firebase:

انتقل إلى Firebase Console وأنشئ مشروعًا جديدًا.

أضف تطبيق ويب إلى مشروعك.

انسخ firebaseConfig الذي يوفره Firebase (يتضمن apiKey, authDomain, projectId, storageBucket, messagingSenderId, appId).

افتح ملف endex.html وابحث عن الكائن firebaseConfig. قم بتحديث القيم بالقيم الخاصة بمشروعك من Firebase Console.

const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_AUTH_DOMAIN",
    projectId: "YOUR_PROJECT_ID",
    storageBucket: "YOUR_STORAGE_BUCKET",
    messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
    appId: "YOUR_APP_ID"
};

قواعد Firestore:

في Firebase Console، انتقل إلى Firestore Database -> Rules.

تأكد من أن لديك قواعد أمان تسمح بالقراءة والكتابة للمستخدمين المصادق عليهم.

rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /artifacts/{appId}/users/{userId}/{documents=**} {
      allow read, write: if request.auth != null && request.auth.uid == userId;
    }
    match /artifacts/{appId}/public/data/{documents=**} {
      allow read, write: if request.auth != null;
    }
  }
}

الفهارس: إذا واجهت أخطاء في الاستعلامات (خاصة تلك التي تجمع بين where و orderBy)، فستحتاج إلى إنشاء فهارس مخصصة. سيوفر لك Firebase Console روابط مباشرة لإنشاء هذه الفهارس. يمكنك أيضًا تحديث ملف firestore.indexes.json ونشره باستخدام Firebase CLI.

قواعد Firebase Storage (لتحميل الملفات في الدردشة):

في Firebase Console، انتقل إلى Storage -> Rules.

تأكد من أن لديك قاعدة تسمح للمستخدمين المصادق عليهم بتحميل وقراءة الملفات في مسار chat_files:

rules_version = '2';
service firebase.storage {
  match /b/{bucket}/o {
    match /chat_files/{chatId}/{fileName} {
      allow read, write: if request.auth != null;
    }
  }
}

إعداد CORS لتخزين Firebase:

للسماح بتحميل الملفات من خادمك المحلي، ستحتاج إلى تكوين CORS على سجل التخزين الخاص بك.

تأكد من أن ملف cors.json الخاص بك موجود في مجلد المشروع.

استخدم Google Cloud SDK لتطبيق إعدادات CORS على سجل التخزين الخاص بك (استبدل YOUR_STORAGE_BUCKET_NAME باسم سجل التخزين الخاص بك من firebaseConfig):

gsutil cors set cors.json gs://YOUR_STORAGE_BUCKET_NAME

إعداد Gemini API Key (الواجهة الخلفية):

ملاحظة أمنية هامة: في بيئة الإنتاج، يجب ألا تعرض مفتاح Gemini API الخاص بك مباشرةً في الكود جانب العميل. يجب أن يتم تخزينه بشكل آمن على خادم خلفي (مثل Firebase Cloud Functions) وأن يتم إجراء جميع استدعاءات Gemini API من خلال هذا الخادم.

للتطوير المحلي، يمكنك الحصول على مفتاح Gemini API من Google AI Studio.

ستحتاج إلى إعداد واجهة خلفية (مثل Firebase Cloud Function) تتلقى الطلبات من واجهتك الأمامية، وتقوم باستدعاء Gemini API باستخدام المفتاح المخزن بأمان، ثم تعيد النتيجة. قم بتحديث متغير backendEndpoint في endex.html بعنوان URL لوظيفتك الخلفية المنشورة.

const backendEndpoint = 'YOUR_FIREBASE_CLOUD_FUNCTION_URL/explainMedication'; // استبدل هذا بعنوان URL لوظيفتك السحابية

تشغيل التطبيق:

لا يمكن تشغيل ملف endex.html مباشرةً في المتصفح بسبب قيود أمان المتصفح (CORS) عند الوصول إلى Firebase وGemini API.

الخيار الموصى به: استخدم إضافة "Live Server" في Visual Studio Code. افتح مجلد المشروع في VS Code، ثم انقر بزر الماوس الأيمن على endex.html واختر "Open with Live Server".

بديل (خادم Python بسيط): في الطرفية داخل مجلد المشروع، يمكنك تشغيل خادم ويب بسيط:

python -m http.server 5500
# أو
python3 -m http.server 5500

ثم افتح متصفحك وانتقل إلى http://localhost:5500/endex.html.

🤝 Contributing
We welcome contributions! If you have suggestions or improvements, feel free to open an issue or submit a pull request.

📄 License
This project is licensed under the MIT License. See the LICENSE file for more details.