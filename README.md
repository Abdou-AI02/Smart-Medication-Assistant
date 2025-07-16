<div align="center">

<h1 align="center">Smart Medication Assistant</h1>

<p align="center">
Your AI-Powered Health Companion for seamless medication management and doctor-patient communication.
<br />
<a href="https://github.com/Abdou-AI02/Smart-Medication-Assistant">Report a Bug</a>
·
<a href="https://github.com/Abdou-AI02/Smart-Medication-Assistant">Request a Feature</a>
</p>
</div>

<div align="center">

</div>

<details>
<summary>🇬🇧 Click here for the English Version</summary>

<div align="center">

<h1 align="center">Smart Medication Assistant: Your AI-Powered Health Companion</h1>

<p align="center">
Unleash the power of intelligent healthcare with the Smart Medication Assistant! This innovative web application is meticulously crafted to revolutionize how patients manage their medications and connect with their doctors. Experience a future where adherence is effortless and communication is seamless, all powered by cutting-edge AI.
<br />
<a href="https://github.com/Abdou-AI02/Smart-Medication-Assistant">Report a Bug</a>
·
<a href="https://github.com/Abdou-AI02/Smart-Medication-Assistant">Request a Feature</a>
</p>
</div>

💡 About The Project: From Idea to Reality
Welcome to the future of personal healthcare management! The Smart Medication Assistant is not just an application; it's a digital bridge connecting patients and doctors in a seamless, intelligent ecosystem. We believe that adherence to medication should be effortless, and medical communication should be crystal clear. This project was born from the spark of inspiration to create a tool that simplifies complex routines and fosters stronger patient-doctor relationships, all while leveraging the power of Artificial Intelligence.

This project was built with passion and precision using these core technologies:

Frontend: HTML5, Tailwind CSS, JavaScript, Chart.js, jsPDF, QR Code Generator, jsQR, DOMPurify.

Backend & Database: Firebase Authentication, Cloud Firestore, Firebase Storage.

Artificial Intelligence: Google Gemini API.

🚀 Getting Started
To get a local copy up and running, follow these simple steps.

Prerequisites
You need to have the following installed:

Git

Node.js (for potential future backend functions, though not strictly required for this frontend-only setup)

Python (for a simple local server alternative)

Installation
Get a free Firebase project and configure your web app.

Go to Firebase Console.

Create a new project.

Add a web app to your project and copy your firebaseConfig object.

Open endex.html and paste your firebaseConfig details into the firebaseConfig constant.

const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_AUTH_DOMAIN",
    projectId: "YOUR_PROJECT_ID",
    storageBucket: "YOUR_STORAGE_BUCKET",
    messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
    appId: "YOUR_APP_ID"
};

Configure Firebase Security Rules for Firestore and Storage. Ensure they are secure (e.g., only authenticated users can read/write their own data, and public data is accessible only by authenticated users). Refer to the Firestore Rules and Firebase Storage Rules sections in the Arabic part of this README for examples.

Setup CORS for Firebase Storage. If you're running locally, ensure your cors.json file is configured and applied to your Firebase Storage bucket using gsutil cors set cors.json gs://YOUR_STORAGE_BUCKET_NAME.

Get a Gemini API Key and set up a secure backend endpoint.

Obtain a Gemini API key from Google AI Studio.

Crucially, this key must be stored on a secure backend (e.g., Firebase Cloud Function). Your frontend will call this backend endpoint, which then uses the key to interact with Gemini AI.

Update the backendEndpoint variable in endex.html with the URL of your deployed backend function.

const backendEndpoint = 'YOUR_FIREBASE_CLOUD_FUNCTION_URL/explainMedication'; // Replace this with your cloud function URL

Clone the repository:

git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git

(Replace YOUR_USERNAME and YOUR_REPOSITORY_NAME with your actual GitHub username and repository name).

Navigate into the project directory:

cd YOUR_REPOSITORY_NAME

Run the application locally:

Recommended (Live Server extension for VS Code): Open the project folder in Visual Studio Code, right-click endex.html, and select "Open with Live Server".

Alternative (Simple Python HTTP Server):

python -m http.server 5500
# or
python3 -m http.server 5500

Then open your browser and navigate to http://localhost:5500/endex.html.

💡 Usage
Once the application is running, you can interact with it using the following commands/actions:

Select Role: Choose to log in as a Patient or a Doctor from the home screen.

Authentication: Sign up for a new account or log in with existing credentials.

Patient Dashboard:

My Medications: Add new drugs, track dosages, set times, and view instructions. Mark doses as taken and archive old medications.

Medication History: Review all archived medications.

My Doctors: View linked doctors, initiate chats, and submit ratings.

My Profile: Update personal information and share your unique UID with doctors.

Connection Requests: Accept or decline linking requests from doctors.

Doctor Dashboard:

My Patients: View linked patients, access their details, and manage their medications.

Send Linking Request: Request to link with a new patient using their UID.

My Profile: Update your professional details.

Statistics: View insightful charts on patient and medication data.

Chat Feature: Engage in real-time secure messaging with linked users, attach files, and set message urgency.

AI Explanation: Get instant, simplified explanations for medications using AI.

🔒 Privacy Policy
Your privacy is critically important.

API Keys & Sensitive Data: Gemini API key is securely stored on the backend and never exposed client-side. Firebase configuration is publicly accessible but protected by robust Firebase Security Rules.

User Data: Patient and doctor data (e.g., medications, profile info) is stored in Cloud Firestore and secured by Firebase Security Rules, ensuring only authorized users (the user themselves or linked doctors/patients) can access relevant information.

Chat History: Your conversation history is stored within your Firebase project and secured by Firestore rules. Files shared in chat are stored in Firebase Storage.

2FA Simulation: The 2FA feature is a simulation for demonstration purposes. A real-world 2FA implementation requires server-side secret generation and verification.

🤝 Contributing
Contributions make the open-source community an amazing place to learn, inspire, and create. Any contributions you make are greatly appreciated.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also open an issue or submit a pull request.

Fork the Project

Create your Feature Branch (git checkout -b feature/AmazingFeature)

Commit your Changes (git commit -m 'Add some AmazingFeature')

Push to the Branch (git push origin feature/AmazingFeature)

Open a Pull Request

📄 License
Distributed under the MIT License. See LICENSE for more information.

</details>

<details>
<summary>🇸🇦 انقر هنا للنسخة العربية</summary>

<div dir="rtl" align="right">

<h1 align="center">مساعدك الدوائي الذكي: رفيقك الصحي المدعوم بالذكاء الاصطناعي</h1>

<p align="center">
أطلق العنان لقوة الرعاية الصحية الذكية مع مساعدك الدوائي الذكي! هذا التطبيق المبتكر مصمم بعناية فائقة لإحداث ثورة في كيفية إدارة المرضى لأدويتهم والتواصل مع أطبائهم. اختبر مستقبلًا يصبح فيه الالتزام بالعلاج سهلاً والتواصل سلساً، كل ذلك بفضل قوة الذكاء الاصطناعي المتطورة.
<br />
<a href="https://github.com/YOUR_USERNAME/YOUR_REPOSITORY/issues">الإبلاغ عن خطأ</a>
·
<a href="https://github.com/YOUR_USERNAME/YOUR_REPOSITORY/issues">طلب ميزة جديدة</a>
</p>
</div>

💡 عن المشروع: من الفكرة إلى الواقع
مرحبًا بك في مستقبل إدارة الرعاية الصحية الشخصية! مساعدك الدوائي الذكي ليس مجرد تطبيق؛ إنه جسر رقمي يربط المرضى والأطباء في نظام بيئي سلس وذكي. نحن نؤمن بأن الالتزام بالأدوية يجب أن يكون سهلاً، وأن التواصل الطبي يجب أن يكون واضحًا تمامًا. وُلد هذا المشروع من شرارة الإلهام لإنشاء أداة تبسط الروتين المعقد وتعزز العلاقات الأقوى بين المريض والطبيب، كل ذلك مع الاستفادة من قوة الذكاء الاصطناعي.

تم بناء هذا المشروع بشغف ودقة باستخدام هذه التقنيات الأساسية:

الواجهة الأمامية: HTML5، Tailwind CSS، JavaScript، Chart.js، jsPDF، QR Code Generator، jsQR، DOMPurify.

الواجهة الخلفية وقاعدة البيانات: Firebase Authentication، Cloud Firestore، Firebase Storage.

الذكاء الاصطناعي: Google Gemini API.

🚀 البدء
للحصول على نسخة محلية من المشروع وتشغيلها، اتبع هذه الخطوات البسيطة.

المتطلبات الأساسية
يجب أن يكون لديك ما يلي مثبتًا:

Git

Node.js (للوظائف الخلفية المحتملة في المستقبل، على الرغم من أنها ليست مطلوبة بشدة لإعداد الواجهة الأمامية فقط)

Python (لخادم محلي بسيط بديل)

التثبيت
احصل على مشروع Firebase مجاني وقم بتكوين تطبيق الويب الخاص بك.

اذهب إلى وحدة تحكم Firebase.

أنشئ مشروعًا جديدًا.

أضف تطبيق ويب إلى مشروعك وانسخ كائن firebaseConfig الخاص بك.

افتح ملف endex.html والصق تفاصيل firebaseConfig الخاصة بك في ثابت firebaseConfig.

const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_AUTH_DOMAIN",
    projectId: "YOUR_PROJECT_ID",
    storageBucket: "YOUR_STORAGE_BUCKET",
    messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
    appId: "YOUR_APP_ID"
};

تكوين قواعد أمان Firebase لـ Firestore و Storage. تأكد من أنها آمنة (على سبيل المثال، يمكن للمستخدمين المصادق عليهم فقط قراءة/كتابة بياناتهم الخاصة، ويمكن الوصول إلى البيانات العامة فقط من قبل المستخدمين المصادق عليهم). إليك أمثلة:

قواعد Firestore:

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

قواعد Firebase Storage (لتحميل الملفات في الدردشة):

rules_version = '2';
service firebase.storage {
  match /b/{bucket}/o {
    match /chat_files/{chatId}/{fileName} {
      allow read, write: if request.auth != null;
    }
  }
}

إعداد CORS لتخزين Firebase. إذا كنت تقوم بالتشغيل محليًا، تأكد من تكوين ملف cors.json وتطبيقه على سجل تخزين Firebase الخاص بك باستخدام gsutil cors set cors.json gs://YOUR_STORAGE_BUCKET_NAME.

احصل على مفتاح Gemini API وقم بإعداد نقطة نهاية خلفية آمنة.

احصل على مفتاح Gemini API من Google AI Studio.

من الأهمية بمكان أن يتم تخزين هذا المفتاح على واجهة خلفية آمنة (مثل Firebase Cloud Function). ستقوم واجهتك الأمامية باستدعاء نقطة النهاية الخلفية هذه، والتي ستستخدم المفتاح المخزن بأمان للتفاعل مع Gemini AI.

قم بتحديث متغير backendEndpoint في endex.html بعنوان URL لوظيفتك الخلفية المنشورة.

const backendEndpoint = 'YOUR_FIREBASE_CLOUD_FUNCTION_URL/explainMedication'; // استبدل هذا بعنوان URL لوظيفتك السحابية

استنساخ المستودع:

git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git

(استبدل YOUR_USERNAME و YOUR_REPOSITORY_NAME باسم مستخدم GitHub الخاص بك واسم المستودع).

انتقل إلى دليل المشروع:

cd YOUR_REPOSITORY_NAME

تشغيل التطبيق محليًا:

الخيار الموصى به (إضافة Live Server لـ VS Code): افتح مجلد المشروع في Visual Studio Code، انقر بزر الماوس الأيمن على endex.html، واختر "Open with Live Server".

بديل (خادم Python بسيط):

python -m http.server 5500
# أو
python3 -m http.server 5500

ثم افتح متصفحك وانتقل إلى http://localhost:5500/endex.html.

💡 الاستخدام
بمجرد تشغيل التطبيق، يمكنك التفاعل معه باستخدام الأوامر/الإجراءات التالية:

تحديد الدور: اختر تسجيل الدخول كمريض أو طبيب من الشاشة الرئيسية.

المصادقة: سجل للحصول على حساب جديد أو سجل الدخول باستخدام بيانات الاعتماد الموجودة.

لوحة تحكم المريض:

أدويتي: أضف أدوية جديدة، وتتبع الجرعات، واضبط المواعيد، واعرض التعليمات. ضع علامة على الجرعات التي تم تناولها وأرشفة الأدوية القديمة.

سجل الأدوية: راجع جميع الأدوية المؤرشفة.

أطبائي: اعرض الأطباء المرتبطين بك، وابدأ محادثات معهم، وقدم تقييمات.

ملفي الشخصي: قم بتحديث معلوماتك الشخصية وشارك معرف المستخدم الفريد (UID) الخاص بك مع الأطباء.

طلبات الربط: اقبل أو ارفض طلبات الربط من الأطباء.

لوحة تحكم الطبيب:

مرضاي: اعرض المرضى المرتبطين، وادخل إلى تفاصيلهم، وقم بإدارة أدويتهم.

إرسال طلب ربط: اطلب الربط بمريض جديد باستخدام معرف المستخدم الخاص به.

ملفي الشخصي: قم بتحديث تفاصيلك المهنية.

الإحصائيات: اعرض رسومًا بيانية ثاقبة حول بيانات المرضى والأدوية.

ميزة الدردشة: شارك في المراسلة الآمنة في الوقت الفعلي مع المستخدمين المرتبطين، وقم بإرفاق الملفات، واضبط أهمية الرسالة.

شرح الذكاء الاصطناعي: احصل على تفسيرات فورية ومبسطة للأدوية باستخدام الذكاء الاصطناعي.

🔒 سياسة الخصوصية
خصوصيتك مهمة للغاية.

مفاتيح API والبيانات الحساسة: يتم تخزين مفتاح Gemini API بشكل آمن على الواجهة الخلفية ولا يتم كشفه أبدًا لجانب العميل. يمكن الوصول إلى تكوين Firebase بشكل عام ولكنه محمي بقواعد أمان Firebase القوية.

بيانات المستخدم: يتم تخزين بيانات المريض والطبيب (مثل الأدوية ومعلومات الملف الشخصي) في Cloud Firestore وتأمينها بواسطة قواعد أمان Firebase، مما يضمن أن المستخدمين المصرح لهم فقط (المستخدمون أنفسهم أو الأطباء/المرضى المرتبطون) يمكنهم الوصول إلى المعلومات ذات الصلة.

سجل الدردشة: يتم تخزين سجل المحادثات الخاص بك داخل مشروع Firebase الخاص بك وتأمينه بواسطة قواعد Firestore. يتم تخزين الملفات المشتركة في الدردشة في Firebase Storage.

محاكاة المصادقة الثنائية: ميزة المصادقة الثنائية هي محاكاة لأغراض العرض التوضيحي. يتطلب تطبيق المصادقة الثنائية في العالم الحقيقي إنشاء سر والتحقق منه على جانب الخادم.

🤝 المساهمة
نرحب بالمساهمات! مجتمع المصادر المفتوحة هو مكان رائع للتعلم والإلهام والإبداع. أي مساهمات تقدمها هي محل تقدير كبير.

إذا كان لديك اقتراح من شأنه أن يجعل هذا أفضل، فلا تتردد في عمل تفرع للمستودع وإنشاء طلب سحب. يمكنك أيضاً فتح مشكلة بالعلامة "تحسين".

تفرع المشروع (Fork the Project)

أنشئ فرع الميزة الخاص بك (git checkout -b feature/AmazingFeature)

التزم بتغييراتك (git commit -m 'Add some AmazingFeature')

ادفع إلى الفرع (git push origin feature/AmazingFeature)

افتح طلب سحب (Open a Pull Request)

📄 الترخيص
هذا المشروع مرخص بموجب ترخيص MIT. انظر LICENSE للمزيد من التفاصيل.

</details>
