
# AthletIQ | منصة تحليل أداء اللاعبين الناشئين بالذكاء الاصطناعي

## مقدمة
تهدف هذه المنصة إلى تمكين الأندية والأكاديميات من اكتشاف وتقييم اللاعبين الناشئين بدقة وموضوعية، باستخدام تقنيات الذكاء الاصطناعي المتقدمة مثل YOLOv8 وMediaPipe لتحليل مقاطع الفيديو.

## المشكلة
يعاني مجال اكتشاف المواهب الكروية من اعتماد كبير على التقييمات التقليدية التي تفتقر إلى الدقة، مما يؤدي إلى ضياع العديد من المواهب. المنصة تقدم حلاً ذكيًا مبنيًا على البيانات لتحسين فرص اكتشاف اللاعبين الموهوبين.

## الفكرة
تقوم الفكرة على تحليل فيديوهات المباريات والتدريبات لاستخراج معلومات حول أداء اللاعب، مثل تحركاته وتفاعله مع الكرة وسرعة استجابته. يتم بعد ذلك تصنيفه تلقائيًا إلى محترف أو مبتدئ باستخدام نموذج YOLOv8.

## التقنيات المستخدمة
- YOLOv8: لاكتشاف وتتبع اللاعبين وتصنيفهم.
- MediaPipe: لتحليل حركات الجسم.
- Roboflow: لتحضير البيانات وتوليد مربعات التحديد.
- Python + OpenCV: لتحليل الفيديو ومعالجة الإطارات.
- Streamlit (أو Flask): لربط النموذج بواجهة استخدام تفاعلية.

## جمع البيانات
- تم استخراج الفيديوهات من YouTube، تشمل مباريات لنجوم عالميين (فئة محترف) ومباريات مدرسية ومحلية (فئة مبتدئ).
- تم معالجة البيانات عبر:
  - استخراج فريمات الفيديو بمعدل 1 فريم/ثانية.
  - توليد bounding boxes يدويًا باستخدام Roboflow.
  - تطبيق تقنيات Augmentation مثل التدوير والتعتيم.

## مخرجات المشروع
- نموذج أولي قادر على تصنيف اللاعبين بدقة مبدئية.
- واجهة بسيطة لرفع الفيديو وعرض النتائج.
- تقارير فورية لتقييم الأداء.

## التحديات
- قلة توفر فيديوهات عالية الجودة لفئة الناشئين.
- الحاجة لتحسين دقة النموذج وتوسيع قاعدة البيانات.
- ربط النموذج بواجهة استخدام مباشرة.

## الخطة المستقبلية
- تحسين النموذج وزيادة عدد بيانات التدريب.
- تطوير واجهة المستخدم وتحسين تجربة الاستخدام.
- دمج المنصة مع أنظمة الأندية لتسريع عملية اكتشاف المواهب.

---

# AthletIQ | AI-based Platform for Evaluating Young Football Talents

## Introduction
AthletIQ is a smart platform designed to assist clubs and academies in identifying and evaluating young football talents using AI-powered video analysis with YOLOv8 and MediaPipe.

## Problem
The current scouting systems rely heavily on subjective judgments, often missing out on real talents. Our platform offers an objective and automated way to evaluate players based on their real-time performance in matches.

## Idea
We analyze match/training videos to extract key data (movement, ball interaction, speed, etc.) and classify players into "Beginner" or "Professional" using a YOLOv8 model.

## Technologies Used
- YOLOv8 for player detection and classification.
- MediaPipe for pose estimation and movement tracking.
- Roboflow for bounding box generation and augmentation.
- Python + OpenCV for video processing.
- Streamlit or Flask for the web interface.

## Data Collection
- Data collected from YouTube videos (professional vs beginner).
- Frames extracted at 1 fps and labeled using Roboflow.
- Data augmented using techniques like rotation, cropping, lighting change.

## Project Outcomes
- A working prototype for classifying players.
- Simple web interface to upload videos and get results.
- Instant PDF reports summarizing performance.

## Challenges
- Difficulty finding clear and high-quality videos of young players.
- Model still under development (~30% completed).
- Need for real-time user interface integration.

## Future Plans
- Improve model accuracy with more data.
- Develop an advanced user interface.
- Integrate the platform with club systems to enable digital talent scouting.
