You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "3rd-Graduation-Day-2018.html",
    "context": {
      "title": "",
      "first_heading": "3rd GRADUATION DAY CELEBRATION 2018"
    }
  },
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "4TH-GRADUATION-DAY-OF-VPC.html",
    "context": {
      "title": "",
      "first_heading": "4th GRADUATION DAY - VPUC 2017"
    }
  },
  {
    "path": "7th-ICSE-Interschool-District-Sports-Meet.html",
    "context": {
      "title": "",
      "first_heading": "7TH BALLARI DISTRICT ICSE INTER SCHOOL SPORTS MEET"
    }
  },
  {
    "path": "8th-ANNUAL-DAY-CELEB-2016-17-CHINNARA.html",
    "context": {
      "title": "",
      "first_heading": "8th ANNUAL DAY CELEBRATION 2016-17 - \"CHINNARA VAIBHAVA\""
    }
  },
  {
    "path": "ACADEMIC.html",
    "context": {
      "title": "ACADEMICS",
      "first_heading": "ACADEMICS"
    }
  },
  {
    "path": "ACADEMICS-CT.html",
    "context": {
      "title": "ACADEMICS",
      "first_heading": "ACADEMICS"
    }
  },
  {
    "path": "ACHIEVMENT.html",
    "context": {
      "title": "ACHIEVMENTS",
      "first_heading": "ACHIEVEMENTS"
    }
  },
  {
    "path": "ACHIEVMENTS.html",
    "context": {
      "title": "ACHIEVMENTS",
      "first_heading": "ACHIEVEMENTS"
    }
  },
  {
    "path": "ACTIVITIES.html",
    "context": {
      "title": "",
      "first_heading": "Vishwajyothi PU College"
    }
  },
  {
    "path": "ADMIN-STAFF.html",
    "context": {
      "title": "ADMIN STAFF",
      "first_heading": "ADMIN STAFF"
    }
  },
  {
    "path": "ADVENTURE-CAMP-2016-17-Mr-Jyothi-Raj.html",
    "context": {
      "title": "",
      "first_heading": "ADVENTURE CAMP 2016-17 Mr.Jyothi Raj"
    }
  },
  {
    "path": "ANNUAL-SPORTS-MEET-2016-17.html",
    "context": {
      "title": "",
      "first_heading": "ANNUAL SPORTS MEET 2016-17"
    }
  },
  {
    "path": "ANNUAL-SPORTS-MEET-2017.html",
    "context": {
      "title": "",
      "first_heading": "ANNUAL SPORTS MEET"
    }
  },
  {
    "path": "Activities-VJM.html",
    "context": {
      "title": "SCIENCE & ART FAIR",
      "first_heading": "Activities"
    }
  },
  {
    "path": "Activities-VPUC.html",
    "context": {
      "title": "SCIENCE & ART FAIR",
      "first_heading": "ACTIVITIES"
    }
  },
  {
    "path": "Annual-Sports-Meet---2018.html",
    "context": {
      "title": "",
      "first_heading": "ANNUAL SPORTS MEET 2018"
    }
  },
  {
    "path": "Annual-Sports-Meet---VJM.html",
    "context": {
      "title": "",
      "first_heading": "ANNUAL SPORTS MEET - VISHWAJYOTHI MONTESSORI"
    }
  },
  {
    "path": "CALENDER.html",
    "context": {
      "title": "CALENDAR OF EVENTS",
      "first_heading": "CALENDAR OF EVENTS - 2019-20"
    }
  },
  {
    "path": "CARRER.html",
    "context": {
      "title": "SCHOOL ADMISSION",
      "first_heading": "CAREER PORTAL"
    }
  },
  {
    "path": "CARRIER-MONTESSORI-FORM.html",
    "context": {
      "title": "SCHOOL ADMISSION",
      "first_heading": "APPLY FOR CAREERVISHWAJYOTHI\u00a0MONTESSORI"
    }
  },
  {
    "path": "CARRIER-VIPS-FORM.html",
    "context": {
      "title": "SCHOOL ADMISSION",
      "first_heading": "APPLY FOR CAREERVISHWAJYOTHI INTERNATIONAL PUBLIC SCHOOL"
    }
  },
  {
    "path": "CARRIER-VPU-FORM.html",
    "context": {
      "title": "SCHOOL ADMISSION",
      "first_heading": "APPLY FOR CAREERVISHWAJYOTHI PU COLLEGE OF SCI & COM"
    }
  },
  {
    "path": "CARRIER.html",
    "context": {
      "title": "SCHOOL ADMISSION",
      "first_heading": "CAREER PORTAL"
    }
  },
  {
    "path": "CLUBS.html",
    "context": {
      "title": "CLUBS",
      "first_heading": "CLUBS"
    }
  },
  {
    "path": "COLLEGE-ADMISSION.html",
    "context": {
      "title": "SCHOOL ADMISSION",
      "first_heading": "COLLEGE ADMISSION"
    }
  },
  {
    "path": "COLLEGE-CHILDRENS-DAY-2015.html",
    "context": {
      "title": "",
      "first_heading": "COLLEGE CHILDRENS DAY 2015"
    }
  },
  {
    "path": "COLLEGE-INFRASTRUCTURE.html",
    "context": {
      "title": "INFRASTRUCTURE",
      "first_heading": "INFRASTRUCTURE"
    }
  },
  {
    "path": "COLLEGE-ORIENTATION-DAY-2016-17.html",
    "context": {
      "title": "",
      "first_heading": "COLLEGE ORIENTATION DAY 2016-17"
    }
  },
  {
    "path": "COLLEGE-PRINCIPAL.html",
    "context": {
      "title": "PRINCIPAL\u2019S MESSAGE",
      "first_heading": "PRINCIPAL\u2019S MESSAGE"
    }
  },
  {
    "path": "COLLEGE02.html",
    "context": {
      "title": "COLLEGE",
      "first_heading": "COLLEGE"
    }
  },
  {
    "path": "CULTURAL-EVENTS.html",
    "context": {
      "title": "CULTURAL EVENTS",
      "first_heading": "CULTURAL EVENTS"
    }
  },
  {
    "path": "CURRICULAM.html",
    "context": {
      "title": "CURRICULUM",
      "first_heading": "CURRICULUM"
    }
  },
  {
    "path": "Celebration-of-Blue-Day-in-VJM-2017.html",
    "context": {
      "title": "",
      "first_heading": "Celebration of Blue Day in Montessori"
    }
  },
  {
    "path": "Celebration-of-Deepavali-in-VJM-2017.html",
    "context": {
      "title": "",
      "first_heading": "Celebration of Deepavali in Montessori 2017"
    }
  },
  {
    "path": "Celebration-of-Orange-Day-in-VJM.html",
    "context": {
      "title": "",
      "first_heading": "Celebration of Orange Day in Montessori"
    }
  },
  {
    "path": "Childrens-Day-Celebration-2018.html",
    "context": {
      "title": "",
      "first_heading": "CELEBRATION OF CHILDREN'S DAY AT VISHWAJYOTHI MONTESSORI SCHOOL"
    }
  },
  {
    "path": "Childrens-Day-Celebration-2019.html",
    "context": {
      "title": "",
      "first_heading": "CELEBRATION OF CHILDREN'S DAY AT VISHWAJYOTHI MONTESSORI SCHOOL"
    }
  },
  {
    "path": "Childrens-Day-celebration-in-VJM-2017.html",
    "context": {
      "title": "",
      "first_heading": "Celebration of Children's Day in Montessori 2017"
    }
  },
  {
    "path": "Christmas-Celebration-Vishwajyothi-Montessori.html",
    "context": {
      "title": "",
      "first_heading": "Celebration of Christmas Day in Vishwajyothi Montessori & School"
    }
  },
  {
    "path": "Christmas-Winter-Day-Celebration-at-VJM.html",
    "context": {
      "title": "",
      "first_heading": "CELEBRATION OF CHRISTMAS & WINTER DAY AT VISHWAJYOTHI MONTESSORI SCHOOL"
    }
  },
  {
    "path": "Circle-Time-Story-Telling-Activity.html",
    "context": {
      "title": "",
      "first_heading": "STORY TELLING & CIRCLE TIME ACTIVITY"
    }
  },
  {
    "path": "Clay-Modeling-at-VJM-2019.html",
    "context": {
      "title": "",
      "first_heading": "CLAY MODELLING AT VISHWAJYOTHI MONTESSORI SCHOOL"
    }
  },
  {
    "path": "Contribution-for-Kodagu-.html",
    "context": {
      "title": "",
      "first_heading": "Flood Relief Fund Contribution to KODAGU"
    }
  },
  {
    "path": "Dasara-Celebration-at-VJM-VIPS-2018-19.html",
    "context": {
      "title": "",
      "first_heading": "DASARA CELEBRATION IN VIPS & VJM"
    }
  },
  {
    "path": "Diwali-celebration-at-VJM-2019.html",
    "context": {
      "title": "",
      "first_heading": "DIWALI CELEBRATION IN\u00a0 VISHWAJYOTHI MONTESSORI"
    }
  },
  {
    "path": "ENVIRONMENT-DAY-2015.html",
    "context": {
      "title": "",
      "first_heading": "ENVIRONMENT DAY 2015"
    }
  },
  {
    "path": "ENVIRONMENT-DAY-2017.html",
    "context": {
      "title": "",
      "first_heading": "WORLD ENVIRONMENT DAY 2017"
    }
  },
  {
    "path": "ENVIRONMENT-YOGA-DAY-2017.html",
    "context": {
      "title": "",
      "first_heading": "WORLD YOGA DAY"
    }
  },
  {
    "path": "EXHIBITION-2015.html",
    "context": {
      "title": "",
      "first_heading": "EXHIBITION OF STAMPS AND COINS COLLECTIONS 2015"
    }
  },
  {
    "path": "FACUALTY.html",
    "context": {
      "title": "FACULTY",
      "first_heading": "FACULTY"
    }
  },
  {
    "path": "FACUALTY02.html",
    "context": {
      "title": "FACULTY",
      "first_heading": "FACULTY"
    }
  },
  {
    "path": "FIELD-TRIP-VJM-2017.html",
    "context": {
      "title": "",
      "first_heading": "FIELD TRIP MONTESSORI 2017"
    }
  },
  {
    "path": "FRUIT-SALAD-COMPETITION-.html",
    "context": {
      "title": "",
      "first_heading": "FRUIT SALAD PREPARATION ACTIVITY"
    }
  },
  {
    "path": "Farmer-Day-at-VJM-2019.html",
    "context": {
      "title": "",
      "first_heading": "Farmers Day Celebration @ Montessori"
    }
  },
  {
    "path": "GALLERY-2015-16-VIPS.html",
    "context": {
      "title": "",
      "first_heading": "GALLERY - \u00a0VIPS 2015-16"
    }
  },
  {
    "path": "GALLERY-2015-16-VJM.html",
    "context": {
      "title": "",
      "first_heading": ""
    }
  },
  {
    "path": "Gallery-2015-16.html",
    "context": {
      "title": "",
      "first_heading": "GALLERY"
    }
  },
  {
    "path": "Gallery-2016-17.html",
    "context": {
      "title": "",
      "first_heading": "GALLERY"
    }
  },
  {
    "path": "Gallery-2017-18.html",
    "context": {
      "title": "",
      "first_heading": "GALLERY"
    }
  },
  {
    "path": "Gallery-2018-19..html",
    "context": {
      "title": "",
      "first_heading": "GALLERY"
    }
  },
  {
    "path": "Gallery-2018-19.html",
    "context": {
      "title": "VISHWAJYOTHI INTERNATIONAL PUBLIC SCHOOL | BALLARI SCHOOL | CONVENT | VIPS | VIP EDUCATIONAL TRUST",
      "first_heading": "WELCOME"
    }
  },
  {
    "path": "Gallery-2019-20.html",
    "context": {
      "title": "",
      "first_heading": "GALLERY"
    }
  },
  {
    "path": "HEAD-MESSAGE.html",
    "context": {
      "title": "ACADEMIC HEAD MESSAGE",
      "first_heading": "ACADEMIC HEAD MESSAGE"
    }
  },
  {
    "path": "HOSTEL-FACILITY.html",
    "context": {
      "title": "HOSTEL FACILITY",
      "first_heading": "HOSTEL FACILITY"
    }
  },
  {
    "path": "HOSTEL.html",
    "context": {
      "title": "HOSTEL",
      "first_heading": "HOSTEL\u00a0& DINING"
    }
  },
  {
    "path": "II-GRADUATION-DAY-2016-17.html",
    "context": {
      "title": "",
      "first_heading": "II GRADUATION DAY 2016-17"
    }
  },
  {
    "path": "INDEPENDENCE-DAY-2016.html",
    "context": {
      "title": "",
      "first_heading": "INDEPENDENCE DAY 2016"
    }
  },
  {
    "path": "INDEPENDENCE-DAY-2017.html",
    "context": {
      "title": "",
      "first_heading": "INDEPENDENCE DAY 2017"
    }
  },
  {
    "path": "INDEPENDENCE-DAY-2018.html",
    "context": {
      "title": "",
      "first_heading": "INDEPENDENCE DAY 2018"
    }
  },
  {
    "path": "INDEPENDENCE-DAY-in-VJM-2018.html",
    "context": {
      "title": "",
      "first_heading": "INDEPENDENCE DAY CELEBRATION IN VJM - 2018"
    }
  },
  {
    "path": "INFRASTRUCTURE02.html",
    "context": {
      "title": "INFRASTRUCTURE",
      "first_heading": "INFRASTRUCTURE"
    }
  },
  {
    "path": "INSTRUCTIONS-TO-PARENTS.html",
    "context": {
      "title": "INSTRUCTIONS TO PARENTS",
      "first_heading": "INSTRUCTIONS TO PARENTS"
    }
  },
  {
    "path": "INTERNATIONAL-OLYMPIC-DAY-2016-MARATHON.html",
    "context": {
      "title": "",
      "first_heading": "INTERNATIONAL OLYMPIC DAY 2016 MARATHON"
    }
  },
  {
    "path": "INVESTITURE-CEREMONY-2015-16.html",
    "context": {
      "title": "",
      "first_heading": "INVESTITURE CEREMONY 2015-16"
    }
  },
  {
    "path": "INVESTITURE-CEREMONY-2016-17.html",
    "context": {
      "title": "",
      "first_heading": "INVESTITURE CEREMONY 2016-17"
    }
  },
  {
    "path": "INVESTITURE-CEREMONY-2017-18.html",
    "context": {
      "title": "",
      "first_heading": "INVESTITURE CEREMONY 2017"
    }
  },
  {
    "path": "INVESTITURE-CEREMONY-2018.html",
    "context": {
      "title": "",
      "first_heading": "INVESTITURE CEREMONY 2018"
    }
  },
  {
    "path": "International-Olympic-Day-2018.html",
    "context": {
      "title": "",
      "first_heading": "INTERNATIONAL OLYMPIC DAY IN VIPS"
    }
  },
  {
    "path": "KITE-FESTIVAL-2016-17.html",
    "context": {
      "title": "",
      "first_heading": "KITE FESTIVAL 2016-17"
    }
  },
  {
    "path": "Kannada-Nudi-Sobagu-2018.html",
    "context": {
      "title": "",
      "first_heading": "KANNADA NUDISOBAGU @ VIPS"
    }
  },
  {
    "path": "Krishna-Janmastami-2018.html",
    "context": {
      "title": "",
      "first_heading": "Shri Krishna Janmastami Celebration in Montessori 2018"
    }
  },
  {
    "path": "LABS.html",
    "context": {
      "title": "LABS & LIBRARY",
      "first_heading": "LABS &\u00a0LIBRARY"
    }
  },
  {
    "path": "LOGISTICS.html",
    "context": {
      "title": "LOGISTICS",
      "first_heading": "LOGISTICS"
    }
  },
  {
    "path": "METHODLOGY.html",
    "context": {
      "title": "TEACHING METHODLOGY",
      "first_heading": "TEACHING METHODLOGY"
    }
  },
  {
    "path": "MONTESORI.html",
    "context": {
      "title": "MONTESSORI",
      "first_heading": "MONTESSORI"
    }
  },
  {
    "path": "MONTESSORI-ADMISSION.html",
    "context": {
      "title": "SCHOOL ADMISSION",
      "first_heading": "MONTESSORI\u00a0ADMISSION"
    }
  },
  {
    "path": "NATIONAL-DAYS.html",
    "context": {
      "title": "",
      "first_heading": "NATIONAL DAYS\u2019 CELEBRATIONS"
    }
  },
  {
    "path": "NORMS-REGULATIONS.html",
    "context": {
      "title": "NORMS & REGULATION",
      "first_heading": "NORMS & REGULATION"
    }
  },
  {
    "path": "National-Youth-Day-2018.html",
    "context": {
      "title": "",
      "first_heading": "NATIONAL YOUTH DAY"
    }
  },
  {
    "path": "Navy-Day-Celebration-at-VJM-2019.html",
    "context": {
      "title": "",
      "first_heading": "NAVY DAY"
    }
  },
  {
    "path": "ORIENTATION-COUNSELLING.html",
    "context": {
      "title": "PARENTS ORIENTATION & COUNSELLING",
      "first_heading": "PARENTS ORIENTATION & COUNSELLING"
    }
  },
  {
    "path": "OTHER-ACTIVITIES-2015.html",
    "context": {
      "title": "",
      "first_heading": "OTHER ACTIVITIES 2015"
    }
  },
  {
    "path": "OTHER-ACTIVITIES-2016-17.html",
    "context": {
      "title": "",
      "first_heading": "OTHER ACTIVITIES 2016-17"
    }
  },
  {
    "path": "PARENT-ORIENTATION-PROGRAMME-2017-.html",
    "context": {
      "title": "",
      "first_heading": "PARENT ORIENTATION PROGRAMME"
    }
  },
  {
    "path": "PARENTS-ORIENTATION-PROGRAMME-2016-.html",
    "context": {
      "title": "",
      "first_heading": "PARENTS ORIENTATION PROGRAMME 2016"
    }
  },
  {
    "path": "PLAY-GROUND.html",
    "context": {
      "title": "PLAYGROUND",
      "first_heading": "PLAYGROUND"
    }
  },
  {
    "path": "PRATHIBAKARANJI-T-L-D-L-WINNERS-2016.html",
    "context": {
      "title": "",
      "first_heading": "PRATHIBAKARANJI TALUQ LEVEL & DISTRICT LEVEL WINNERS 2016"
    }
  },
  {
    "path": "PREFECT-SYSTEM.html",
    "context": {
      "title": "PREFECT SYSTEM",
      "first_heading": "PREFECT SYSTEM"
    }
  },
  {
    "path": "PRINCIPALS-MESSAGE.html",
    "context": {
      "title": "PRINCIPAL\u2019S MESSAGE",
      "first_heading": "PRINCIPAL\u2019S MESSAGE"
    }
  },
  {
    "path": "PTM-FOR-ANNUL-EXAM-2015.html",
    "context": {
      "title": "",
      "first_heading": "PTM FOR ANNUL EXAM 2015"
    }
  },
  {
    "path": "PTM.html",
    "context": {
      "title": "PARENT \u2013 TEACHER MEETINGS",
      "first_heading": "PARENT \u2013 TEACHER MEETINGS"
    }
  },
  {
    "path": "Parent-Orientation-in-VJM-2018.html",
    "context": {
      "title": "",
      "first_heading": "PARENT ORIENTATION PROGRAMME IN VJM"
    }
  },
  {
    "path": "Pulses-Day-at-VJM-2019.html",
    "context": {
      "title": "",
      "first_heading": "PULSES DAY @ VJM"
    }
  },
  {
    "path": "REMEDIAL-CLASSES.html",
    "context": {
      "title": "REMEDIAL CLASSES",
      "first_heading": "REMEDIAL CLASSES"
    }
  },
  {
    "path": "REPUBLIC-DAY-2017.html",
    "context": {
      "title": "",
      "first_heading": "REPUBLIC DAY 2017"
    }
  },
  {
    "path": "RESPONSIBILTIES-OF-PARENTS.html",
    "context": {
      "title": "RESPONSIBILTIES OF PARENTS",
      "first_heading": "RESPONSIBILTIES OF PARENTS"
    }
  },
  {
    "path": "Ramzan-celebration-in-VJM.html",
    "context": {
      "title": "",
      "first_heading": "RAMZAN CELEBRATION IN VJM"
    }
  },
  {
    "path": "Republic-Day-2018.html",
    "context": {
      "title": "",
      "first_heading": "REPUBLIC DAY CELEBRATION 2018"
    }
  },
  {
    "path": "SCHOOL-ADMISSION.html",
    "context": {
      "title": "SCHOOL ADMISSION",
      "first_heading": "SCHOOL ADMISSION"
    }
  },
  {
    "path": "SCHOOL-BAND.html",
    "context": {
      "title": "SCHOOL BAND WAGON",
      "first_heading": "SCHOOL BAND WAGON"
    }
  },
  {
    "path": "SCHOOL-CAMPUS.html",
    "context": {
      "title": "SCHOOL CAMPUS-BUILDING",
      "first_heading": "SCHOOL CAMPUS &\u00a0SCHOOL BUILDING"
    }
  },
  {
    "path": "SCIENCE-ART.html",
    "context": {
      "title": "SCIENCE & ART FAIR",
      "first_heading": "SCIENCE & ART FAIR"
    }
  },
  {
    "path": "SCOUTS-GUIDEs.html",
    "context": {
      "title": "SCOUTS GUIDES",
      "first_heading": "SCOUTS, \u00a0GUIDES AND NCC"
    }
  },
  {
    "path": "SMART-CLASS-ROOMS.html",
    "context": {
      "title": "SMART CLASS ROOMS",
      "first_heading": "SMART CLASS ROOMS"
    }
  },
  {
    "path": "SPORTS.html",
    "context": {
      "title": "SPORTS",
      "first_heading": "SPORTS"
    }
  },
  {
    "path": "SRI-KRISHNA-JANMASTAMI-2016-17-VJM.html",
    "context": {
      "title": "",
      "first_heading": "SRI KRISHNA JANMASTAMI 2016-17 VJM"
    }
  },
  {
    "path": "SRI-KRISHNA-JANMASTAMI-2017-VJM.html",
    "context": {
      "title": "",
      "first_heading": "SRI KRISHNA JANMASTAMI - MONTESSORI"
    }
  },
  {
    "path": "SRIKRISHNA-JANMASTAMI-2015.html",
    "context": {
      "title": "",
      "first_heading": "SRIKRISHNA JANMASTAMI 2015"
    }
  },
  {
    "path": "Sankranti-Celebration-in-VIPS.html",
    "context": {
      "title": "",
      "first_heading": "SANKRANTI & KITE FESTIVAL"
    }
  },
  {
    "path": "Saraswathi-Pooja-.html",
    "context": {
      "title": "",
      "first_heading": "SARASWATHI POOJA"
    }
  },
  {
    "path": "School.html",
    "context": {
      "title": "VISHWAJYOTHI INTERNATIONAL PUBLIC SCHOOL | BALLARI SCHOOL | CONVENT | VIPS | VIP EDUCATIONAL TRUST",
      "first_heading": "WELCOME"
    }
  },
  {
    "path": "Science-Exhibition-at-VJM-2019.html",
    "context": {
      "title": "",
      "first_heading": "SCIECNE EXHIBITION @ VJM"
    }
  },
  {
    "path": "Swatchh-Bharath-Campaign-2018.html",
    "context": {
      "title": "",
      "first_heading": "SWATCCH BHARATH CAMPAIGN 2018"
    }
  },
  {
    "path": "TALUK-LEVEL-VIJNANA-BINDU-PROGRAMME.html",
    "context": {
      "title": "",
      "first_heading": "TALUK LEVEL VIJNANA BINDU PROGRAMME (MATHS WORKSHOP)"
    }
  },
  {
    "path": "TEACHERS-DAY-2015.html",
    "context": {
      "title": "",
      "first_heading": "TEACHERS DAY 2015"
    }
  },
  {
    "path": "TEACHING-FACUALTY.html",
    "context": {
      "title": "TEACHING FACULTY",
      "first_heading": "TEACHING FACULTY"
    }
  },
  {
    "path": "TRAINING-MOTIVATION.html",
    "context": {
      "title": "TRAINING | MOTIVATIONAL PROGRAMMES | TEACHERS | STUDENTS",
      "first_heading": "TRAINING & MOTIVATIONAL PROGRAMMES: TEACHERS / STUDENTS"
    }
  },
  {
    "path": "VET.html",
    "context": {
      "title": "VISHWAJYOTHI EDUCATIONAL TRUST",
      "first_heading": "SRI VISHWAJYOTHI EDUCATIONAL TRUST"
    }
  },
  {
    "path": "VIPS-Calendar.html",
    "context": {
      "title": "ACHIEVMENTS",
      "first_heading": "School Calendar"
    }
  },
  {
    "path": "VIPS-Christmas-Celebration-2018.html",
    "context": {
      "title": "",
      "first_heading": "3rd GRADUATION DAY CELEBRATION 2018"
    }
  },
  {
    "path": "VIPS-New-Year-2018.html",
    "context": {
      "title": "",
      "first_heading": "CELEBRATION OF CHILDREN'S DAY AT VISHWAJYOTHI MONTESSORI SCHOOL"
    }
  },
  {
    "path": "VIPS-re-opening-day-for-academic-year-2018-19.html",
    "context": {
      "title": "",
      "first_heading": "VIPS RE-OPENING DAY FOR ACADEMIC YEAR 2018-19"
    }
  },
  {
    "path": "VISHWAJYOTHI-PURASKAR.html",
    "context": {
      "title": "VISHWAJYOTHI PURASKAR",
      "first_heading": "VISHWAJYOTHI PURASKAR"
    }
  },
  {
    "path": "VISMAYA-7th-ANNUAL-DAY-CELEB-2016-17.html",
    "context": {
      "title": "",
      "first_heading": "\"VISMAYA\" - 7th ANNUAL DAY CELEBRATION 2016-17"
    }
  },
  {
    "path": "VJ-HOSTEL-INAUGURATION-CEREMONY-2016.html",
    "context": {
      "title": "",
      "first_heading": "VISHWAJYOTHI HOSTEL INAUGURATION CEREMONY 2016"
    }
  },
  {
    "path": "VJM-BLUE-DAY-CELEBRATION.html",
    "context": {
      "title": "",
      "first_heading": "VISHWAJYOTHI MONTESSORI BLUE DAY CELEBRATION"
    }
  },
  {
    "path": "VJM-Calendar-19-20.html",
    "context": {
      "title": "",
      "first_heading": "School Calendar"
    }
  },
  {
    "path": "VJM-Calendar.html",
    "context": {
      "title": "ACHIEVMENTS",
      "first_heading": "School Calendar"
    }
  },
  {
    "path": "VJM-FIELD-TRIP-2016.html",
    "context": {
      "title": "",
      "first_heading": "VJM FIELD TRIP 2016"
    }
  },
  {
    "path": "VJM-Field-Trip-2017.html",
    "context": {
      "title": "",
      "first_heading": "Celebration of Blue Day in VJM 2017"
    }
  },
  {
    "path": "VJM-OPENING-DAY-2018-19.html",
    "context": {
      "title": "",
      "first_heading": "INTERNATIONAL YOGA DAY IN VIPS"
    }
  },
  {
    "path": "VJM-RAKSHA-BANDAN-2016--17.html",
    "context": {
      "title": "",
      "first_heading": "VJM RAKSHA BANDAN 2016 -17"
    }
  },
  {
    "path": "VJM-SHRI-KRISHNA-JANMASHTAMI-2017.html",
    "context": {
      "title": "",
      "first_heading": "FIELD TRIP VJM 2017"
    }
  },
  {
    "path": "VJM-VIPS-Teachers-Day-2018.html",
    "context": {
      "title": "",
      "first_heading": "CELEBRATION OF CHILDREN'S DAY AT VISHWAJYOTHI MONTESSORI SCHOOL"
    }
  },
  {
    "path": "VJM-YOGA-DAY-2016-17.html",
    "context": {
      "title": "",
      "first_heading": "VJM YOGA DAY 2016-17"
    }
  },
  {
    "path": "Wheat-Day-Celebration-at-VJM-2019.html",
    "context": {
      "title": "",
      "first_heading": "WHEAT DAY @ MONTESSORI"
    }
  },
  {
    "path": "YOGA-DAY-2016.html",
    "context": {
      "title": "",
      "first_heading": "YOGA DAY 2016"
    }
  },
  {
    "path": "academics.html",
    "context": {
      "title": "",
      "first_heading": "1. FACULTY"
    }
  },
  {
    "path": "beginning.html",
    "context": {
      "title": "BEGINNING OF AN ERA",
      "first_heading": "BEGINNING\u00a0OF\u00a0AN\u00a0ERA..."
    }
  },
  {
    "path": "contactus.html",
    "context": {
      "title": "",
      "first_heading": "CONTACT US"
    }
  },
  {
    "path": "css/11f4cdad199790d7cf8da1b1970250ca.css",
    "context": {
      "path": "css/11f4cdad199790d7cf8da1b1970250ca.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/5e3a198b9f557dce8bcf744d800929a9.css",
    "context": {
      "path": "css/5e3a198b9f557dce8bcf744d800929a9.css"
    }
  },
  {
    "path": "css/8262bff05c67ad10ca65768309857ff5.css",
    "context": {
      "path": "css/8262bff05c67ad10ca65768309857ff5.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/c7b031b0f249b5a0e4b4ea5b3f74587c.css",
    "context": {
      "path": "css/c7b031b0f249b5a0e4b4ea5b3f74587c.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/ea877be10548ee44a23888a5c36d402e.css",
    "context": {
      "path": "css/ea877be10548ee44a23888a5c36d402e.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "holiness.html",
    "context": {
      "title": "BLESSINGS OF HIS HOLINESS",
      "first_heading": "BLESSINGS OF HIS HOLINESS"
    }
  },
  {
    "path": "imgs/0004f92ba7bb196543fa6b78cf997988.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/000c4f43de41527787de403025c4ed0e.webp",
    "context": {
      "refs": [
        {
          "alt": "INVESTITURE CEREMONY",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/001a5809e06225fc2ebc63736037255f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/001dcce5da3474bc25955f36558d3921.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/002379ea1b4398cd33530a8511280665.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/003b28a57cf7dfac4f8a6bf3d576fbb0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/00404cb25d1ca7a0698afbc5eeda0203.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0049158d356d52b6ee1b2847026e68c5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/007622813fb6ab54761e408ae0250d03.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/00cee82b60a1d553ef2b1722ea57ad14.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/01063eacbf9559129323d12e70e720c6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/01096987e9c581048b704a81b19b5713.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/011ad85a319e94597d9c47e7ee7063af.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/012bbb1fd271274db9a8ef8e11be0b78.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/01602367eaea43281d255a950933d8a7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0189823945d6148b9f21d805bfcbd739.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/01b18c1f2a3d726e97b2b5f2b9274078.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/01e51dd269c5af1f40be50d1deab45cc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/022c9c8d01f9f439efd3b873aaa7c300.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/023a741ebeafc389bcfb7bf3d2dad883.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0260b2bd7d6627eda77933a24b34f9c1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/02a4ba2c2e83d212ca4c3363c5a323f6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/02c0196aa0045a1aa6828b8521e7964c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/030669781ab512b2875c2d23fe61fa72.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/030e20179c52bef566b860b619129255.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0328ce76c52f6065ec20bb31d0c61a13.webp",
    "context": {
      "refs": [
        {
          "alt": "DiningHall",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/032c504ca11e91f25cca13111d26d6bb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/034d747424c0fbbe73a78944ac227e1e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/039f2b36c4d54eec827b0ed1e046b268.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/03fa5149487437e0bcd50e271b172540.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0409c66ba6d1b4db45a084ab66d2ba0c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/045f9dab07dccbe6f950a3a9359f3e1b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/046faf34a00b999f686475d546a592b4.webp",
    "context": {
      "refs": [
        {
          "alt": "Children's Day - Montessori",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/049f087f96027b6feeda249f2dea418d.webp",
    "context": {
      "refs": [
        {
          "alt": "vipsPreUniversicityFlyerkan",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/04e44d5e3436da13f36d65695083ffe1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/050c372ad53ceb39020e405273b5af57.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/05bc490491b761e6d15344982682ed59.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/05f48c6593918d394950af3622790300.webp",
    "context": {
      "refs": [
        {
          "alt": "School",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0610fc6a74aab032e364b95cba327877.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/06893aab69c6b3e10e11bce9fc9daa8d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/06cdf7fb30aa7f319f8c78139a512b1d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/06fa657b620806a3d4005dc644433ca0.webp",
    "context": {
      "refs": [
        {
          "alt": "Logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/071dbacc93fa4944b8505cf7ab18ae5c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/075a72c11b806d05f7f23849c1e62e9a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/07bbe7f0c597dc4d4be279a6fd7368da.webp",
    "context": {
      "refs": [
        {
          "alt": "Divya jyothi Puraskar",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/082b6484502791baa2affd9cbcc6231b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/085523680dca2c8a90f08e0ee8c31c7d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0862792c6db8171ef8056379fee27ef5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/08ed5bd47341d505456e83587a18ad16.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/096c2eccae1a0b5e55f5adc29821eafc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/09a3db12d503bc043d7e0c46dcd411d9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/09d6aeac4908bcd16a5c0a5cacd3329a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0a0080266f1d09eca43e838116b341f7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0a14c13667b62756418c59946b57cb22.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0a4f15e14a4577527d73983407c1b0d8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0a68d868d4e6a96851e0c44b3b0f9ae5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0a891ea0545f1bef6583dedc61044be5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0ab370575e85c4656a1dbd5b2db526aa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0ace9e1a95fcd5605e973153b2f29e9f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0af5714ae06ab4d08a15a68834124ade.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0b31c11db4ddc04f72b8f6f7d802e6d0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0b674c10cab4f285dbca82f3ce29cbfd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0bcd1a250a28190ab4e5ac7645b4eb68.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0c064f61da5bc90745c5356974c98f45.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0c162b1c01b41f9d6a4687036165966a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0c3f8b78d3f2860118dc4b9430714667.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0c83839ebe6a1a6f1419bd45cb5b3e00.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0c8d5946c19feac0873a0aa22b00ff03.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0cd86f8799497fe3936586d4d97fe4e6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0d472c954d377cb161a7a7f71a8f24a3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0d47bc77cd2af216451827847d70f81f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0ddc4aa8648ff18e4d6c940a15b97e70.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0ddc6680887486d14370b5f94842d9bb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0e38fe45d293aad63a3cc25d1177ad22.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0e6300e7c48202e23af9ebc3462dd852.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0eaa6e4fd9cba3502124bc1d6b22f7d0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0ebef064dfc6cb12616f5f35462266cf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0eccfcaa725041a17a42161860163ccc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0f131ce45aacbae386c1efa5f27bf1bb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0f207d4982e34be8dd142fac8c9c1dea.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0f484ade81b8325eea788456e8916163.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0f488857d81c8314847f8928e03b76e4.webp",
    "context": {
      "refs": [
        {
          "alt": "VIPS Awards & Rewards",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0f70d09ffbbe21649ada724555a68351.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0fd6f57b456d9087a91b818e8d77f5f3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0ff999255ef31ee67ced8d6a8fff6b9d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1020ed11dfaeae9758070d234aaad684.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/10621922cc6bef641dd6a857e4eb2583.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG6545",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1071a06c36b4eddad0808ce627b67589.webp",
    "context": {
      "refs": [
        {
          "alt": "Academics",
          "title": ""
        },
        {
          "alt": "ICSE Curriculum",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/107dc9bd5092498575ebd9c2a52b9106.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/107fdc4e26d75a88ee4994b487f04e3e.webp",
    "context": {
      "refs": [
        {
          "alt": "BIOLOGY LAB",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/10d21b0eb590cc343085ff962693f760.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/112247803190751f0b6245ee6c2e0b59.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1133a025cd522081914699c922facbf6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1141b45a3fa1da8f6eebb94e4a2d1118.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/116c897ef7ba356bd9d611a6f4981d97.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/11f85f1566b24f3726e598c31389010c.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG9405",
          "title": ""
        },
        {
          "alt": "PARENTS ORIENTATION PROGRAMME 2016",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/125da6c31b1a98800f4f4fcb57c22540.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/126f9726ebf64a18b7596b3878cbc1da.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/12df9a142a6f76cc20dcc8456c74418a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/12e64480f8933b97703b00d207b735c0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/12f2f5d34132a5752a4ecf9bdf931571.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/139e288e1646bfeebc72b3d85b6a21f8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/13da762263fa40391d50fd8eb7c105ce.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/141ea4e8c7b81aba877d43730423ff6e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1421d87b897d90f5038c6b007dff4265.webp",
    "context": {
      "refs": [
        {
          "alt": "VISHWAJYOTHI MONTESSORI FIELD TRIP",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/142c99dd5c388065ac4f5486487db307.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/14937710fa498b90c086ad039d7ef6d0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/150c7211e5bc7469fca2bb474c4e992d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/151feafecbb69fa93b5db420c5a5a6ee.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/15424e43b7b17450f7fe56dd68f0bd80.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/15448da13e1f91c744d062480732857a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/15538eddf39801e41ffd3acf82ddb898.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/157f0143bef84346c2f9158edb91e9c7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/159aab98987a56396b4f82e1d879ec43.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/16817427b82ed2767b325ab4bbf8d9d4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/16a92abafe44066e02dab45293bbdd69.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "WHEAT DAY @ VJM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/17136cce7cdf3f22aea1af03168bb538.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1746a5de67d5addfc756b7dfe8715476.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/176fb83aaaa581006bd98ac979f798ec.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/177e567b7dd072b90643e3d404af5793.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/17ac6e3ad786f999e3da825425caa487.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/17e25d553db059ef5ee2c16c36c8113e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/182bde8263d374995e232245c8d36002.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/188c2cc5a6392064eff3116713e7aabe.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/18b722be61d547083fb8c5253f28242a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/18dab38c455dce63ea65de9b6b86c2d1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/190d0d9601f047f4b73aad97022b12ad.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/191585cb0634ba9631d6c8f7ec86f677.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1917ddc96dccc2ac5e756e60a40a885e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Girls are not permitted to:",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/197d865d068df6da1aa0edd64ca8c4c7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1996903ef600a20a129013cc33c57cf1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/19a5d3261ca157a5479f78b2dc3e0468.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/19cb8c3279de747a65f410f6b96a3a9f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1a175c861e2a4b30896c81c32ddde150.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1a6cb023d6b568025d2a7849ec015dc1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1a7580aa446234ef1943b76a0ce417e4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1a88f79ca5ba04dde0c60586044ea643.webp",
    "context": {
      "refs": [
        {
          "alt": "DiningHall",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1adecb82146d870bdac749374ad5e7d4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1ae7a9437590214df60b2b4e30dcd736.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1b8ef5ad09d32b25bf745e04e2fda7f8.webp",
    "context": {
      "refs": [
        {
          "alt": "Father's Day Celebration @ VJM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1bcc6a529512cb9414f081f97fb87511.webp",
    "context": {
      "refs": [
        {
          "alt": "SCHOOL BUILDING",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1be506edf0f5ea8ca783283733609590.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1c1d61d6da8fd942c66e88c1c21f463a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1c465786a60d0cae1b68aee54e43d8a5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1ca202139bcfac0cdf487215603204bf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1cc809ff6eede8ef90ffcde2ded6871c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1d046f9c9cdd898f6f6fc6aae1363862.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "PTM FOR ANNUL EXAM",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1d0c32338755e788f812a1759ffbe6c6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1d39736a3356f62f7ef127a815fd4bb1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1d8fb5feed8ff07eaaaed2760e966c68.webp",
    "context": {
      "refs": [
        {
          "alt": "ATHLETICS/VOLLEYBALL/ BASKETBALL/CRICKET",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1dd9f34ae13e2187e8d6ccf22c1ff68b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1df8c89c38af0063335a37d600ec64b2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1dfaa2dfeaef38697dfa3fb21cf17620.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1e95c72454acfb7a2381bcc346f438ad.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1e9ba04d4218dfd642c28b283f1231e7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1eae31917eb0fa02c4b406fdde80e47d.webp",
    "context": {
      "refs": [
        {
          "alt": "VIPS SCHOOL UNIFORM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1ec244de7bd9ac93281dea012f304625.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1f029f2c83d5d59d35f59aa4b5796ea5.webp",
    "context": {
      "refs": [
        {
          "alt": "PARENTS ORIENTATION & COUNSELLING",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1f27e15a269187e4a360c5e3fad323f3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1fba94fb5aa9a8548fe5c03a03a64bf6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/20164e02cce256c1c8bfd84d3498fb4d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/203bdcfe568491d5a852afe6e5751c1d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/204a59af8e014c429e181c176211257c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2076b8f86800b72082214a522b26c21b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2132cdd06ed80a2c54b3fd75100b1f8f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2143b9be721c2f0565e923b3462389b1.webp",
    "context": {
      "refs": [
        {
          "alt": "Tiger's Day Celebration @ Montessori",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/216c3a5437b2b28309b77e760d0d45b4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/21aa7ccf8861cb73cb3562181dd4f7d6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2200c6044e8a4545d2809fac31b4fee9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2215a85bc2eb53d9183111e4a4f994ad.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2258e7d51ce60db3b632b9817b1285f8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/22595b7538d8665f09a6510b3c71d885.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2261794c08cd75582fb51baa4bd1428c.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG0489",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/22991d357a6144fc4c6b70f04df7c55b.webp",
    "context": {
      "refs": [
        {
          "alt": "INVESTITURE CEREMONY",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/22bdbc852eb905915d037a5b9f731a64.webp",
    "context": {
      "refs": [
        {
          "alt": "Logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/22d456e0562338676cd0a5de818f1948.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/23058cf368200731b1aada9c888bad89.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/23277c4a4bea40cf3437a739c0ae2e9f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/233e184cd865820dd16f4eb4517ad67f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/233fbb497c4e460b43a6c23992a38015.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2371ef7b674043965ada54e03d9c3b4d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/239c62e86679a717ceefe1df8cff6963.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/23f84d63ceb652891177a707dd586d7d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/248ef26e207af40141972d087704557e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/24b438ed74fded9327f1aa70f2f9eaf3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/25241e3c2d5227a3c2cbb7af9c7caa21.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/253f23922019a6c10791866bb6242e9e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/254e3f13d3d13a8a03d0ea7f439fc6ee.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/255228d1b0bdffd19c00fd39abdb8f26.webp",
    "context": {
      "refs": [
        {
          "alt": "DIWALI CELEBRATION IN VISHWAJYOTHI MONTESSORI",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/25591d28e8e789d967dd7652783842f2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/25a1fa120f88430714f7a4b09ffb82cf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/25a4b021b65dc4aee3c994e0d08e07c0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/25a5d9ecc69e5c30637b4cc5ec12f76e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/25dcce1487c1aaf2ca5008fd98de6b54.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2600cb2f727ee02e1bd7147e754ef3e5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/26150ebeda1e4bca4cf23288615dcecd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/261a4fa992f44270672a8f4f75f7054a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2622e37a7bbdb64a05605bcec5771f37.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/26a5de0a4289c21d676f9e69ec35ab77.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/273f198ad7b1312fef3d9673e5fe5de0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/276a9a24ffb5af1ec7b8840c065c758d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2781d9a53a9ff6e832919a41ff27e27f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2795d1dc7452758493186f00127d7c57.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/284ff45430d96c4e6cee75288baed371.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/28a501ed3ee5e34c56fc90f6ea85d678.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/28ff8ebd5dbd922bf5dfd4bdd93e7f21.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/29314e1d85bf97c8d819f226534df769.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2960e0fe6f316f6f210db56a43a3b90e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/296973f6c3938cc197d6aa2676a4a52b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2981a3b595c900f335c1e6cbb008d791.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/29842805cdcc69033de143c542b05bcb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2990680ccddc35ebf8adcf5e513379f2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/29930e5ccf9da9b50c347d361d70818b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/299aadf6e007a2f22ca5710fc08c341f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/29a0a2e72f361a45e1f7030a239eb347.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/29ad835bae0657f8954adddf06969044.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "School Term",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/29d9822dd2288c11ea3215c494a2a6cf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2a1283097855ebbdd8118e516b632747.webp",
    "context": {
      "refs": [
        {
          "alt": "VJM YOGA DAY 2016-17",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2a6f8496ac35a31b37419f0e0c3beb26.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2a70f2dd4bc2c0b743e98ea0aeb70f09.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2a903c07985eec7969bbe5d24c227c8b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2ab4e0f4895b4ce8fe39f914962f9b0a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2acf6ca7121d2b0e8b021268480a5b3a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2b17061b7563b399bb94bdd8ab3300f7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2b2967a54c3dcf2a225d29aaa83d29c7.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG4656",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2b431ee27b9b99b8625061f43dcdf0e8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2b52128650ee272de7afa5bd5735e649.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2b83d6ee97c2b0c8d1356fa7ad9754e7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2b923ab49ccd15ed5c6d523f4a6ee9cf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2b936357042ae088be9a738a07b50f20.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2be7da4d2b07b82b76a429d34418825c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2c0967d7a82a770eb6d99e541c67e15d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2c21815e33ff54af22d92171d571f21b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2c394c5861cff57def4680f367bc245c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2cc503e90fc7e81e13ff9f01890c1d01.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2ceb22e1eeb6afe89893881fca9eaf35.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2d19a4debb50308e6f38686f5566bea0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2d45c9959857398f294913e2ab1d905d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2d5bf58f46dfbb1046ae253c1430ab04.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2db85ed78bfc984c8e30e72589b02ce3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2dd28a4c012f5fa7bcb814186629fba2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2df34d60d6a6a2c360e6e4d60415abee.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2dfb216332715e31e4c8ad689c567dfd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2e11e60394f994bfb7cb908031a894e1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2e3e1a4e53f0f37806430cfa642b28b4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2ec3bf928ef5ed845f98ddb2605e2eda.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2f4002898e17d7e02a7132b0b6141e76.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2f429fa6efbb030c800f678c5adddb90.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2f53a5412754ec73096293b05317b760.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2fdd9453d28ba75f64129db28d1759c0.webp",
    "context": {
      "refs": [
        {
          "alt": "Pre-Nursery Opening Day @ VJM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2ff68d37f9bb0b68280eec1033ea76d2.webp",
    "context": {
      "refs": [
        {
          "alt": "NON-ADMIN STAFF:",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2ff6ecafb088ae9f468fdd6bb0a7d7b1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2ffa57f5539759fc5800e16a1498276c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3005f9c5ba9d5a1ef481a602d51bcf07.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/30297fceb879bed55fe2f2d0ef22ea93.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/302cbb038b02ce45c6133b0c1b2bdf53.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/306481f57814db3fcff72de705c0d487.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/30b9418a67c10743b96a15a593a1cf90.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/30eaec1032273f21d7e2a3d4d566585e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/30f550780aa96636bd0d9c5345353b19.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3107d7a983b026659b0ae5af104bf12f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/310bb5dc4258ad227a714934ea62a70c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/31202dd8a62fd6d563dac7686bf1e53f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/312401ae7058dbfaea7690cdd2501dda.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/31327c7cb0f55be4451dc6ee9db97afa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/31712c7dd9aa46e84d801d4f7ae89244.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/31822780db23fc5e07222f6978792dff.webp",
    "context": {
      "refs": [
        {
          "alt": "Montessori",
          "title": ""
        },
        {
          "alt": "ICSE council",
          "title": ""
        },
        {
          "alt": "IMG",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/31c7361d2ef46c0a7683a28186f182e5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3235fdc5f022061024bf89f74e20e2d0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/324755193fab191ddfcf43c10b31347f.webp",
    "context": {
      "refs": [
        {
          "alt": "TALENT SEARCH AND CAREER GUIDANCE ORIENTATION PROGRAMME",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3248b43ef97324dc8ca73743b47d5b07.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/32c4ced7481a756bc5b0c53b6481933a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/32e438d97408afbf45b9414182d57a7e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/32f94d07bed2b3e907439cad1ced49cd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3309c1752a97eea59ffde250a3ab4cc8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/336150905b83799f6c6e7502c3ad72e7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/33c7fa0c6c2b4bcf3e242339898ae257.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/33d0cfb2598bfcef50e702bb98044a00.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/33eb12b0a4969d9a64346201a3b7bcde.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/33f2602d6ecaaa7a8bd502130a75867b.webp",
    "context": {
      "refs": [
        {
          "alt": "LIBRARY",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3418296d16dbc1d09d170a90d0593098.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/347c756972095684eda035abf3c716c5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/34e3a6db7a8f5e9bf5d50dc61c5f6ea2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/35215c06354c8253c50a659d149c134b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/354b9f1ab9eb6a6116a0687ff7c6887b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/35e34bba47e3b04de6077644777df0bf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/35f64e3371b15d82e5fd52cf33c85a21.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/362d45bbe5c94255ea1408e0097abf89.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/363eac48d4f106ed0d92b8ab7c3998ed.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/36446dc07f4cafe6837d70b13fcc0cca.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/36a680bf6b1c1aa6a29965e00a29bdaf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/36bfdbadfeae00aef5c9e8fda9196ba6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/36e9c919905a736e97adadc219911135.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/377f01d15874d70000fc3da7ebff7368.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/37c3e3717995ef6def0b228154c9de23.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/381b2a7740804392bdcece24164fca12.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/38277bff9d276b3ebfd0d310e2751454.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/38303b8a12251cc6c98341fa096069c1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3870b0a6993c3de47c7cfa316c5fd8fa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/387b19ed83dd0e415ec0c410b9201fce.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/39411eb62973a25babff23d9c76cb1a7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/394366843386988edfc7ace52369dd65.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/396830699b5da3bdec4cc02f642bd010.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/39875b6cf40896aa623d4d41e38d4e42.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/39bff442de9291d41dcd791931b35b93.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/39ca7648350145c58ab9855ba24aaa2d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/39cc147bd12b9068b1b904834ac16765.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/39dc2b139a9862a50b480267cc936121.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/39ea89b9ec092872890d5169de9ccf6d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/39ed4ac63660c6233543c296ac4390bc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3a176dd2f9747ee0addd4d324922824f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3a1ef810f189751a1864985ec5b3c15f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3a1f8c5ff1b9d03ed4ed89a2e07aa0dc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3a3c3e74664dccb2097421f79887fcc7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3a8585a52b805bd43d696087b4791d69.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3b3f106242da574a3b92fdb576e0febf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3be94c1ee1787cd9ea4f3fd935858847.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3c3fb60b2bfde66658dcf2c4b0caaef3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Celebration of Blue Day in Montessori",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3c4635c370ea8b2d55cd8fb83ef2efda.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3c479648629a3c89c47bd5e537c052ed.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3c899ddd2672bde0326a4b5274f7e8ce.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3c8e0541199d5900c1d5f092b3c6d24e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3c904f7afd25eb17816d7784d0855bc1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3cb0774e4a4bd3256756d7fb690fa6a4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3cee4b0cd8a2061bc2fd143ad0422f1f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3d0af22dfe0cc8e2b7583e132f0aee8f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3d23b6d67b36bb439fa45cc5d56d805d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3d827913f9b67fe67b261aae640fbfe6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3e1a43065cec16593ea99524fa953e65.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3e3d8fec48fd2639d88cf1c7a6388ce2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3eb461bedca838cd4a3ed3feb815c4ff.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3ebb4b080fa186c064bf56a4a38d6fcb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3ed9768c5f56f069186ed0bc8e283e76.webp",
    "context": {
      "refs": [
        {
          "alt": "SRIKRISHNA JANMASTAMI",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3f34369aacf7c33b8cf090cc58e2b5cb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3f6b829a60996c6b4c13fe57030af945.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3f9e5cb6564b00827c33564ed169030b.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3fbe2b30a64d24f6d876280c26f0a8ed.webp",
    "context": {
      "refs": [
        {
          "alt": "PULSES DAY @ VJM",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4016c4e8a2cc41094b364fe06d81c9bd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/403cbe18cc33bd3182e7810fdff745ab.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/40833464c7228f242eb97a06ec560800.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/409132700d2f5b397855fbf7f78e8c3c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/40a8f6b587ed1ca08c7ff84f0084207c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/410d0a89ac14b7c26370450700b61446.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/410ddf58811f654c49b97af7fb78296b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4112548ae0424f4f5ad5ac168e6e4aa7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4183925abd395cfc17c54d3eba1444d8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Celebration of Sankranti & Kite Festival",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/41873539253c4e31820f6e68fd9dda7f.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG9809",
          "title": ""
        },
        {
          "alt": "IMG9809",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/41b24cd642a30c2057024e20a145d66f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/42198f885d9080f2bdd30590ded8f241.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4282f6ef34022f81a90fed0e71e7c9e1.bmp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/433514167d2bbf82f28729f3b2df749e.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/438602b3267242fe2caa23d824ac07c7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/43894d2a4ba3d06d6912494313163075.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/441f0954132116aa83c9a94bda1c184b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/446f5b49d256234d6901800452f85f30.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/446fa4cabed2b27d59dcf5e3d24c6a8a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/44eedf78f400697c85f813e20d9ac6cb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4523736bc1186d82e558855135433d64.webp",
    "context": {
      "refs": [
        {
          "alt": "Banana Day @ VJM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/453623a5ae1c0c4c1f51a90fef282ab6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/453d26b5ed9ad2f26e7479cc74a6525b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/454b25b8e9130d32024e2466e3f6318f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4552ca0a8e1f9e6e5ddc920841dc2492.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/45828e2b9c7d67b9111442f8e66b0b4d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/459797592450eb67386c126769125834.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/45a42591a3aacf658530d823e55b306a.webp",
    "context": {
      "refs": [
        {
          "alt": "73rd Independence Day Celebration - 2019",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/45da657ae2f73136438fb951b3d4d764.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/45e798038f14f61bc5c68748745844ca.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/46317ef808759af3719e2b036cb65a30.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/46379887b74cb0fa237c243d39174f5c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/468a63177a7d8ffb6eac82caf5671555.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/468cacab769e10cc1d39e918174bc3e8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4697b3ffcf4435b41dc6196517790657.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/46c6cc9797a066ee4d3bdba92638d48d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/46e00f9d8d289f2055cce91d3351a950.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/46e832414f3e113a42d6a1a11835aebb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/47189dace5a48b4a7e74a800e794686e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/47251046402cd55e31f830a42f6fd890.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/475424781aabdaaa8878a55003f69ba2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4757cbfb4938eafec6e1e5a3df42d0b3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/475fc8c693285f61705356c89ba60af1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/47763de0c96291d83474778b07191b44.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/479bb8593025305e8261edad70b15ccb.webp",
    "context": {
      "refs": [
        {
          "alt": "Celebration of Christmas & Winter Day @ Vishwajyothi Montessori",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/47b19315c35d4fc9712fdbeddf3fa7f1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/47bb99af15d0aff2fa6bef45f9f2552f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4818754e8ee5d232249313cd4992bc98.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/488c70ae6a612def7725cf2b87567f2f.webp",
    "context": {
      "refs": [
        {
          "alt": "Annual Sports Meet 2018",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/48a1e63fc93b1ac5a52a476c7f5d91ab.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/48a90b48430d9749eef8a964b4f62487.webp",
    "context": {
      "refs": [
        {
          "alt": "SRI KRISHNA JANMASHTAMI 2016-17 VJM",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/48bffc7c9460e0a2d77edaa0e88a9bf8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/48c87e10f03334230fa8ed30fa6e5146.webp",
    "context": {
      "refs": [
        {
          "alt": "ICSE council",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/490da35a3896958b996429a071da1475.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4956e6583eb348142cae90ade6f5af7d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/495a71cef1c713521e46f5993b905e2c.webp",
    "context": {
      "refs": [
        {
          "alt": "Logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/495c5e6ce51b3d3ca5788e63665700a6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4969e54edf95289459323903c23b76c5.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/49b2f3291ae72205ff6bfbfddad2ed4b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/49c5da20a46009f881a80b3ae9ba3aa4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4a2aa8b33565336bc75e6fdd083fcd55.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4ab160d28e3a26645ea60a22818f6cf7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4ac17b077b808d7e02dc0fc346a9b635.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4adb9f480ebb4cdca1a3bff859212d37.webp",
    "context": {
      "refs": [
        {
          "alt": "Welcome to School",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4af9c4f0f0964de41953c81c9790cc78.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4b4426f377b9e980168c31998882c562.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4b993765bc48a671a1ca02474da597d4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4bdeb11775718ed03ab26b4a772e0057.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4beed4cccf4648db60bc3c606489d895.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4c1d89c68e086ee429e393b997ee4cac.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4c3c759299284d700847293ce4f00b3a.webp",
    "context": {
      "refs": [
        {
          "alt": "7th ICSE INTERSCHOOL SPORTS MEET BALLARI ZONE",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4c4d909c169438938c872cc0012833f0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4ca22d35144d3c4ee5a78f9cf813adab.webp",
    "context": {
      "refs": [
        {
          "alt": "VISION",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4cd105a7264e641f16e139f581c0494d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4cdc2d08aa6fcaee3ee8389bc0561b27.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4ceb3a0bba8a58da93377500b903663e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4cee0fb1ebab2cbbed53b26eb81d8400.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4d0610b0b46cf3c1fa232a935bd14eba.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4d16628c99b13c94f02cb901f626408f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4d37e0073b536cd17e7196dab920496f.webp",
    "context": {
      "refs": [
        {
          "alt": "KISA Utsav 2019 - Zonal Winners & Participants of Regional Level",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4d8b32e3a706dd37766146a5fb856a76.webp",
    "context": {
      "refs": [
        {
          "alt": "HampiPhotosElephantStableHampiHampi114931jpgdestreviewimages510x3411324603607",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4dd196bb52fe603ae803daaeb451bc27.webp",
    "context": {
      "refs": [
        {
          "alt": "DiningHall",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4eeb6419085dce383b2d6b6130b9c86a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5018b880a101b41c56c5f70b20d4f240.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/50599ed55750cd325fa211b2dea3c692.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/513c8ff30541370eaba1b7f9b8aa3ab5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "WORLD ENVIRONMENT DAY",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/51d8c655b4698f832c7ffbb6125c342d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/51e41af72d112ff059e1fce4ec697b69.webp",
    "context": {
      "refs": [
        {
          "alt": "COMING SOON",
          "title": ""
        },
        {
          "alt": "COMING SOON",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5288312c792eb5e2bd1434d592adfcbd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/530518e7f356016905487ad32574df8a.webp",
    "context": {
      "refs": [
        {
          "alt": "Children's Day",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/532ba959661b97a84406bfcf95093a57.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/53bd376f1f90cc5efbc099266629be72.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/53c77004b653fbe927c5999b8c1407bf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/54aa71b9699e25ee226bc97a010782eb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/54d2ee00cad05518d50b2ad3260164db.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/55004b783f70dd9e370a1319b6591862.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/551e6d498f852d02e869c1acf296057f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/554981c0f6afe19dfd1346eb69da2636.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/556b1d623e3b474487d31e2395f589bf.webp",
    "context": {
      "refs": [
        {
          "alt": "FOR BOYS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/55ed2898ad2844b111cce33085f0e485.webp",
    "context": {
      "refs": [
        {
          "alt": "DiningHall",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5659b1f1bf923794e2d894ac82d08396.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5659d5a837a5e5680751a9592300c58f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/57002bc96e26815f2b65a64e7c85a5e0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/570a4964d285d09ca71d1ee47efd4380.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/571d406c8aea5996206ebfc6c13fee6c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/572755bb10d0475a9f16f52fd4cac796.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5730e923131882aece56131ca54574bb.webp",
    "context": {
      "refs": [
        {
          "alt": "School Re-opening for the Academic year 2018-19",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/57540e33249a9d3816ed5b16d8db0cf8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/57850c268af8ecc0064ae19da107b737.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/57871c98d4dff197aee7ef189156fdf1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/57abda55ac85c1a2457baa374cafb029.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/57b549168e2819b7b36b6fc4bcd40e18.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/57f91fb965bd2ac9b9bfc3473a1f6bec.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5845dbd034e51a78b3b5c99c4e9b6474.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5858ac35aa21192de5b7ec8ac1aed334.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/58846b497f4194f3e38bbfcd458f103b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/58b750072cf0ae62ed91171a840a356d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/58e569a582c68e8a5bdb4e20cde9140b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/592ab4a022bc76b4799e84f33f522071.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/59898ab05fdab5c18343f137b0cdc003.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/59baa0c0f6c0cb37312190721d244f62.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/59ce43e7379c8ea736c6b1aa56ddd2e0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5a1f5117e9daa27db19c1cad5819496d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5ab0c8866c47182d6a9d80b866acb374.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5af1b7a5180c1bb392eee8f66dc37427.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5b08ac8d9962a005bdc0191b1e468cdf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5b0e596c004e7f5d41237cca135b1d07.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5b4aa090e97778e76b70f1afbe3be81c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5b7070795d34d770e3c790c6e8a5396c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5c0924388f744a916167fcf51a511a2f.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5c3cc738475230bec7f2088b01fc8413.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5cc9ac7845019c830c21812662a4fca3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5cc9afe6897f1a3e08961b63bce6686c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5ce0b79f76e060557a5845e433571684.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5ce54c217633523c0e9808b7d7fe5cb2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5cf5ac0d27ddb88bbf3786eb01846f97.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5d53751075fe1ba0265d7205d178f382.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5d685bcdd9804896811ee8bca188e5e0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5d75495b593346b81a7046aff10e7d4a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5d7754442f3f35edf8122204d3ed219a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5de4cabc0da48b456a8cd2d436dffef4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5e06c37b073f6fd666618cc775e18b44.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5e54a144b924ee11bbe80ad14e6e6a7b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5e9b9f4f3607eeafe35862b1e4ceb4ce.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5ed4cbc87df0b3b562ccbdbda1d5efed.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5ee130b6080c3acead08ab5d96a13d46.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5ee4928753bca246e712fda77d1863c8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5ef72a09ec1ae7eb157b6bf46343e629.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5efdeee80637a2f8810fca813ffd3d82.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5f4e28fece44f187227184826fa5d711.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5f5c0a06b42c9377ac5a7f7214318703.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5f5febd26a97929b5dfb111aa97dff9b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5f6a1ab58607aefd347f09411d5ca98f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5f76bc39a951f0f91c1491ed7ab9dc62.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5f80135fa55d648fd566a6cd20f68664.webp",
    "context": {
      "refs": [
        {
          "alt": "Blue Day Celebration @ VJM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5ff6a5b0d553e30aefefbf9c25b30482.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/603049ad4dde4a8ce8b5e810bae26e7f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/606921dfb2fd4c57f781c25447ed9163.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/607b81e74d80f322371c0ea647111b38.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/609175ffdec5013d59db38e86dd27b63.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/612cf110d96f97faf2d9710c90ca5f77.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/613b68bcbc453256e66c610f281a8e90.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/615e1e18bc8031251e95a44e68c10b01.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/618076292b4edf72cc29846103a9767c.webp",
    "context": {
      "refs": [
        {
          "alt": "DiningHall",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/61985c00488af7de812e3f3ae6bd2b14.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/61f6ae1ecfdaeb86e8a2ebbaef20323a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/620a964688dccde49486c6a4334e862d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/622716fe1cb3a48f9cebde78cd46cb5f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/62974627f57d7823deff537b837d8ab9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/62ca846bf16f8cc4ab923dad8096864a.webp",
    "context": {
      "refs": [
        {
          "alt": "BIJU",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/62e41aa66c6752e6469d79b4002a7f91.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/63343631c6794cf5a52c354113cdc89a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/634090c33e50eddce7d4cc24e3297028.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/63602e3e0526897f668120b24bd5dc12.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6360e569bcd8356f18807c6e794b737f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/637caf09afba5d3ac69b27956cf7d074.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/63a3e0d499251a6150b83b3e8259c3ba.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/63cb797e4d32e41d6d83e3df7393da3b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/63f965cb4bd27b7434a6542df8b17767.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6402a082b98482d59d2359e32656e93b.webp",
    "context": {
      "refs": [
        {
          "alt": "Doctors Day celebration @ VJM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/640e610752ff300f08fba7242535bb80.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6423fadd0e4001c025375b5d72eebadf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/649faf39c50c0142e4d6ab4b90b26401.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/64a88780a9b0f7a0ed1152c2b91aeba2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/64d2330ce4d5df290670dd0cd59a1a2a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/64da34a82476b5ab982ba91623e5788e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/64ef0c9c3a7df18a03e8222417409177.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/651c0420a265aecd0d46a9a9a298f328.webp",
    "context": {
      "refs": [
        {
          "alt": "FOR GIRLS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/65b1271c8bd7daa7c3b866fdfea4800d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/65be3c2f0f56a622992a5c27c34b084a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/65bf9663aea1b89b450e520f2bc9e45a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/65d29473590b81735122a429521ff0f4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/660e8c7b4224f3d7c251443d5a206e60.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/664814936746eca9af734aa80f8d485a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6654b5a13650cc81ebc6072e2544a005.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/666fbe2d44a225d9bd6f5486513e97f1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6681445eacc0446d57b836c1928615b5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/66baec3b4d700a95ca757137acb0e559.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/66ddf649747444ae88ed34ed0f28265d.webp",
    "context": {
      "refs": [
        {
          "alt": "School Uniforms",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/66f97173169af213b9b52eba3e31bd2c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/674680bc46e3f7201bcb969e8b4ff9b4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/67468c264bedce26b379ea8e500fb3d7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/674cd8dd0033880d80348fe62309ca06.webp",
    "context": {
      "refs": [
        {
          "alt": "PUC",
          "title": ""
        },
        {
          "alt": "IMG",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/67c3fc339de55cac578cb633ca4275fd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/67d979526164ee5b1687ce18e465309e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/68a7ad05503b7346c95cbaa1f00d68a0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/68a8064466d924962c618fe73fa38321.webp",
    "context": {
      "refs": [
        {
          "alt": "INVESTITURE CEREMONY 2016-17",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/68b1b5f580cab6bd626bdcae9f92fcda.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG9817",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/68d23ce3e4d28cdecd8b392d0f2ab971.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6966c804aade9dc61cd3b188505374cf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "CHILDREN'S DAY (VJM)",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/697ccfcb317306c9716e319c23be135d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6a5437fa5e2238ce84789a49292b557a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6a5ac16f29a7f7dc1d86dd1526d548ae.webp",
    "context": {
      "refs": [
        {
          "alt": "ROAD AT CITY",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6a78c32c50cc3ccf69464c25357f1a4a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6ac4058a6f697ee0654d901b60c201c7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6adaf4b6b0cf76ea824c5c9cadfcc6ac.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6b1129baf3f8557bc29c41d4dfc4f46d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6b392eff410ac7de971da49496c0104b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6b63c42e888ae50505fa0e07180acae8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6b91d1cfb3a71bfa84f1c0fd99053302.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6ba1caf82e0d510a24ce0fea2ba6e449.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6bae9b4e67d51c41554411c055021d4b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6bc26a8a6817d894b6840be28f6ab93b.webp",
    "context": {
      "refs": [
        {
          "alt": "IMGCopy",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6bd9dc1a4cf0e2ca56143dfe55069757.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6c01703f57fbb9d9b74cae0e107497f4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6caef636ac3ed97d14270761ea91057d.webp",
    "context": {
      "refs": [
        {
          "alt": "CHEMISTRY LAB",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6cc39db43ec653cdd4b567a008cc68e2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6cccd93152aa50db10c91b82221f1bb9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6d028c31542e1986f2c49bb3a5af31ba.webp",
    "context": {
      "refs": [
        {
          "alt": "INTERNATIONAL OLYMPIC DAY 2016 MARATHON",
          "title": ""
        },
        {
          "alt": "IMG9405",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6d08fa5013c68d36db8750c09b17087f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "SHRI KRISHNA JANMASTAMI MONTESSORI",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6d773d2e464fe246b367635d8c8ee92e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6dab730ae2464a7f52f3b25c144054ac.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6db9fa22ce852e5bc1abd3840561bb9f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6dc7b91725c90724ae2de875f30fd2f8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6dd8268bb0f6215d96664277de9cee29.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6def69db8d1eda0531647245acb886e2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6dfbb118f2d4615c40d75a91faee836e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6e2c4351e413f09c8eb1bfcc82bbace5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6f1809421a5a904200cfa2601990b2b6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6f2139752ab26b7e2507bbd9220e2b67.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6f66b8c32345dfe9d238eccbc2be0db2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6fc4e00600e789e7a589b9696813e622.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6fd2e5b2d8f0d315ef7535a2a0392e25.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6fe73cd500d7523f60e21c562ccc192d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/701bafbd3c38fd53cf8e1e99c1e10b67.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/704eb090c5c28cd993cdc37db0e9b4cb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/706de580ea16bc22593665ee4d6668fa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/70863c140c68b97571cf14b95b6c10af.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/70ef7544ee531cad9adefdac9369f32b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/71070bb8d1436e1d9d3e9490662e2644.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/712a9214e5eaae83e03f3f073a7e0497.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/71680838aef2377d63f1eb69746b6117.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/717d31bfbb0bd105071b519747ea71e1.webp",
    "context": {
      "refs": [
        {
          "alt": "VJM FIELD TRIP 2016",
          "title": ""
        },
        {
          "alt": "DiningHall",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7182ff7040256fb9402595a1888755a1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/724e8fa918c5156aebdf8d4d8c299ea9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7266e3a8f88c8b4e94a6b007bb05cfab.webp",
    "context": {
      "refs": [
        {
          "alt": "INVESTITURE CEREMONY - 2018",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7290e113f8444d611694ec6cdc628902.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/72b91d2a250073e67087d444cbb1eba7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/72c452456861fb9eed3930b916a0d01f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/732250e9898352508bb4ecd8ba36cba1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/73354e38f966a32d8005b1131b2e4742.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/733b602a6a92ff47117e44a83d015bc7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/741231f958755092594b874aa8d0b849.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/74234679e1ff23e6c771f39e9f32c9a0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7487837227a25b37549d7dc0b1100651.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7488979a2c88da05630f8431a9580975.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/74ac3bdb3edeaebbb0c04b6625d889fc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/74fcceb43fd10f5a96aa92c86067c7e2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/74ffbb0c7e1ef06e022ffbd0810602ee.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7593c966b6702c34147b01cbb0f35357.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/75e58b64eb69480173b0b7c8c7890057.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/75f5142893a802abb83a91f7f2671fa7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/76565440355e9f92c800b4b92760636c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/767a516f0ca7663a353b70d1457b52d7.webp",
    "context": {
      "refs": [
        {
          "alt": "DiningHall",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/76a4059d3805fadbc98096300e1423a7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/76b47e958ec11f42c99201b3e60754f1.webp",
    "context": {
      "refs": [
        {
          "alt": "d7da8a5d4632b804e7ab9e9fbf19bbde",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/76debedd3d0c1eddf1b6561f3d0be2d9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/76f91b411cab11f81b736be933e3c18f.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/770095fcae5694618f8c03f4518623d1.webp",
    "context": {
      "refs": [
        {
          "alt": "FIRST AID",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/773d3a9811dc9346b5abfcf733091d82.webp",
    "context": {
      "refs": [
        {
          "alt": "School Re-opening Day - 2018-19 - Vishwajyothi Montessori",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/778ea1056468aca24222055ef052ccc8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/77ab81b8f65916208b6afddeeb5504c7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/77ae4420daa4e6e6fb74dac4ecf8d3c4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7823e8a83582c69e26f4a66164635826.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7875e83ca01f286dc1047f332bdcff94.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/788393c651c77b7bc8d1668b70934db6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/78bd81d938a7c0c63794ac03c3e537a2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/78e629a21951cf790e021a720f83eec5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7902a1576f7251069a15a4d3e2370ef4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/79184937f23b225cc01d33745bfc6c1f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/79913faaa9ede7d3daf53061176742ef.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/79d64070f17012628dc97e4b0678c53f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/79df9eefb9fb9fffb4aa4e1e6c491a35.webp",
    "context": {
      "refs": [
        {
          "alt": "VISHWAJYOTHI MONTESSORI - BLUE DAY CELEBRATION",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7ae30611927b5e644864a4df989fd4cb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "CLAY MODELLING @ VISHWAJYOTHI MONTESSORI",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7b0b59a85596ece7e7b1bd6384266c05.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7b2cd86d26bedba5dde24891e0334262.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7b524ece5acff74132bbcada7962d71e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "SARASWATHI POOJA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7b7247ab08501063ffc2dcce3dd78d28.webp",
    "context": {
      "refs": [
        {
          "alt": "KITE FESTIVAL 2016-17",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7bb093152ed1b14169005f236fce745f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7bbbdddeb5ce233a72fc367252cb31fa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7be5d3fdc0ce4767670e56ac3462bf64.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7bf2b2a2aee743d1474d64cca0773a4f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7c396fa8d83b3c4d3f6d23c0f45615ca.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7c4e7424fa75466eb944640df75e9f93.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7c7467f6c530571a21b51d7c80ad1841.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7c9853c42482b4311f995a811105ddbb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7c9ad4d96787eb117c986fd19237e153.webp",
    "context": {
      "refs": [
        {
          "alt": "DiningHall",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7cbd3cbb6c0871e8253bcad2794c9d02.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7cbd7616e933bd133ff39194788fb0fa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7cd21429693be568f3e6d157476ac138.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7ce9f93bcc1644b0379ba38d3e283413.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7ceac878f69b2509c8ec198456d9ae79.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7d03d1705338854594ddada5732dbdff.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7d050777b265fecc69aecd70542e485a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7d0afef16752b1dfa348d3aaf6bf8cf4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7d38e7e5ccb5ca4330d232a67c80f6db.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7d4bbbb270b47172a0d8cfe1745ed787.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7d4f21d40c2afeef1f0e27f52dc193d8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7d6ddf44f3b9d642f74cad7464f8a115.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7d71d3e01cff7fd4c22509b6c8749ebe.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7d82e7a69cb7ab8d516d1f24f616d6a0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7d91f238412f9b7b75fffd29fba9ebf2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7d98d8b4bce850d128930a53b841dfb6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7da102c3c80a42c988256f2207d4f560.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7dbc9d441d16b6676d75c73dd923a2c2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7de6758a412b6c75fd2a7197e81a5c6c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7ded738c9520c3e24a78d7eab9f493e9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7e5b25c9f5716084c635a6af607dc35c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7ea01248a120814b1f9268590a4b7b0e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7ebabb1687f00e9557e6aec238163afa.webp",
    "context": {
      "refs": [
        {
          "alt": "FOR GIRLS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7ed5a3ecf20d557884c7e794cf653ec7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7f3315250eeabc7ceeaec481cef53ed6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7f394dde0afab4169663c8a824423693.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7f3e9167df205450e3dfa9f33adabc6a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7f4d5dbc4d36c83cee5061af4e7cb0d8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7f50925a4d4c1d9fa4ae8a4446a0c38d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7f629c63ab765079e9083bfb1cd7dd60.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7f6db4f455cc98f34d1926105f4e5dd5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7f77a91bc21ffca207196b556feb0bba.webp",
    "context": {
      "refs": [
        {
          "alt": "INTERNATIONAL YOGA DAY",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8028294fca8b378986d15cbbf116f3de.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8032bebe09b0131cc8161ec977ef0ac5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/805c390b590d49ee37dc4e24109cfb97.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/805e10d1c7cdd3bcbf8e347c34bd4acd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/80751a6dbc3c892fa056df2dcdb0006f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/80df9bea94922e03d5119bf600284ff8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/81237a0968c6c02d6e6a2fe9eb14afc8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/81d11950e5fc2d375eed16562181a806.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/81dfbc6c96910a4803ee8cfa0b640418.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/82cae3d5745462b907ef5c35fcf4f0e7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/82dad92d935efc002065037e6c7e0894.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/82de74c220d1ecb39ed5d72918a160d8.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG0489",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/82edae6380be7726917e269d2858e5c0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/83087829dd79cec9c32d7f7bef838467.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/831b3c3b749a17ed5e2b93343c237fb1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/833cc9d53d51348cba32812c200669a0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/83786570395bf9dad5481d3c38431a77.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/83caf7d58e121e7c4ace9b8ab06f45bf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/83e370043177f2c5ba2d7219b5680769.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/83e88afbe98cdf115472a855fbd2b5a7.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG0489",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8450a9c928e6d4d1408bf040d3a0f28e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/847b4324563b6ceed7a5ba3f0bf22790.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/84987f13ddf0cb0ab66cfdf0896df0b6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/84c28bc3fa0ade992b4823a0e80bb82c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/84e5ead56d9c02fca17f04f3070232b2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/84f8df7f2da89e043465767ce2c008d8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/856fee26c938072ae6a0f5b044bb325f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8579d39025ed220b3bd7c9001237eba9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/85d782438e8e992d8f8246c9be3af0b0.webp",
    "context": {
      "refs": [
        {
          "alt": "TeachingStaffwithManagement",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/85d94fbe853e661db3a25ab7cc66cd63.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/861b0c5424dc3f7d7287ab162f00ce9e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/865b0274ae501704a78298cd90b9e5a9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/86601a1d2c6399343f84087fae40cdb2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/86a43a89f39002f7ff4a5da51844a488.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/86a97684f1ffdace5052c3ca5670660b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/86b06bd245fe23548d7b43ca14b821d3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/86c66bc5812ced855e700b3c5315645b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/86c89b3c8d4f5db5781c24a5ba97e8c4.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/86c8b80059bd8e407a7915a007118df9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/86edabc7060e3003b05155541454be79.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/87038135dd7553aba5c440230762b453.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/877cc919d9169cf5260615af251f1bbf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/87b210dc77241bd06aeff21bc440e058.webp",
    "context": {
      "refs": [
        {
          "alt": "8410886529fd9ae52206b",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/882d0ab41e0e630e1a9cd3b0f8b57525.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/88328153bd53b8a58cce0e72611ba2d9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8834fc54432d14458f22122ea451ab9c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/886a7796ba2b5a233a3865626e5fa20a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/886fd06fb78f2efb1fbfb1407872c2cb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8887dfad0013487bfcbcd6f650af428a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/88886c553a5f798715958aa9b41ac7a5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/888d62acc882a7ee1ef26abf3b2a6bfa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/88cd179b690ce67eb4364ea93cdb55c9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/88e2d973ef7c10cea9b652f82a9c1e55.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/88f64a63f274d0d7f693f306e240c507.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/895560e9c4a9fab32d3122daf5e10d7b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/89938faaaa1dab9d85f92ad805f3ef54.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/89d820fbf2c61daec339e3871d386be4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/89e02fd10c1ceb85b009b1ab360bc68e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/89e3962470a656b73fbab1fa51286390.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8a192a9a0012b6a6247504f240433e73.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8a52af7d3f71fbfadf478eaed1f71258.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8a7338370602426e88490c6f67e10688.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8a983e262db7ce3145762e21c8c8224b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8aa1a60d3abaf237b4dadc7fca04f185.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8ae0e5228e6f77036c1a1498e028d7f2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8b0046e8bee3cb350f575f8527d9d8ae.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8b261c480d5db7f695947289b66f7dcb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8bb06db21c63dfdf52a56e868dd428d1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8c28ec3f4e951439ec563790b05ca0d5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8c5f17c8f9d447021eb954e6036775a3.webp",
    "context": {
      "refs": [
        {
          "alt": "DSC",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8ce31d8c64b9133155856091ca4a3b67.webp",
    "context": {
      "refs": [
        {
          "alt": "VIPS school foundation, Vishwajyothi",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8ce56a338bb267f2a13a6857c221e530.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8cec046988a40e25694e6917971ff6d8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "National Youth Day 2018",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8cee48eed18f9de0d1551d68ea0fbf2c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8cf85edd8be16a7dcd3a4a28680d0542.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8d060d05acee01d1eb90090d2815d7c8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8d28c3ab9b60ab0597ebda8c2313fc58.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8d6c9464c82e3d1275a96412751b91ef.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8db149d3c2c6571ce559ff624079db38.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8db76a9fcc68f77566b75fe3bb34c9b1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8dc847cf9d337dea6ffdfe319a9ab8ef.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8dec57f9ebc913fcce40e2c9df00a3e3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8df690412ada808459367007796b41f1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8f3b9f5edda72b139a7f532062f50446.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8f60fbbe2e5d075b2ececeab19eba69d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/900c4a6642f3c93d2833bf8c8b9b20d1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/901fc60a28acb0716b5446cd1fc3a40a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9024627ee2dcd735bc0e88a1ef5f7c19.webp",
    "context": {
      "refs": [
        {
          "alt": "YOGA DAY 2016",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/905c8fa8248d4c5f8cfab959bbf480d6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/909d7368723d31dc350cd7133ad76449.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/90b8e83ed6d2d29165ea2cdc1bc93463.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/91356e51be5bdb1953a194954aecd554.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/913af8dcbcec41ab343490bd96d0d358.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9142a05f41042f3617515844b444ebc9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9142cdc0f3f1b972dce6c9cfcae7f453.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9156d78839f1ba3d26bd781fbba1ba8e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/919a899e76bc934c3954f4c1fad60f7d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/919fea3cd2bccd277a7edb26d8acf4e2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/91ad64c95f363fd5c39928352182d570.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/91c3ec340ac35f871c9cdb951958b8d2.webp",
    "context": {
      "refs": [
        {
          "alt": "Swatchh Bharath campaign from VIPS",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/91e495d6e852a7dd306a4d3bd0c9004f.webp",
    "context": {
      "refs": [
        {
          "alt": "DiningHall",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/920e8775acc277e2735aa9bacc3ffd82.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/925f998fa93f1e49679d2a0fcbdfe310.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/92aed835ab8758cc557e45831249a8e3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/92c2b459ebf3196f3c274af6ba752e1b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/92db3878062881a1135033a9b0d096ff.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/93452cf639d313f11904c2aedf0fd951.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/935f5ecaf593e6e4b4455d3ee6e0065b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/937c765793b619ca6292d706f53c6c21.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/93e9fd4a42bb68747dccea4b7e4a3041.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/943af8b332e0d976ea58e3216f06b745.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/944892b3db3453d767b1246f57d82395.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/945422386b2108433896e1bf7f8fed20.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/94b136b7881f0392ae3ea8b8596f5db2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/94b7e51de319a0920d29ddfb6de796a4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/94e6d983850dea820b38ea58b745feea.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/951127463afe14ed21d5cfd67eb183a2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9598a9b7051417162b28e041983b3b49.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/960e968be6d2343f614acba7a062d8f4.webp",
    "context": {
      "refs": [
        {
          "alt": "LANGUAGE LAB",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/96158e6c0df561400b05d10e3134b01b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9647f1c528b0304daa67c3c0ed244445.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/96a41a77681cbcb928f554977c7064e5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/96b74b6cab797f09d89b010395c92483.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/97568acc8dcaf846659c80bb97b712c1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/979df9f83a9d4b4829c0fa6f124541dc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/984a3209400767fcee01a48a15d7deea.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/989cb1c7729a738c4422afc99089cb3a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/98fb5e4968a49141c035846405620591.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/991633c2809599812f1de62a901676fd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/997666d96cc2e96bae8deb64f29cb761.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9a29866ac1156b19f2f48410143faa72.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9af48041a3055c987064d17d829967fd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9b3468af93b52431f520b6aade879847.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9b53b10e4a0136ef234bed651ea921ba.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9b593856f1009135fafd473c09125ed2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9b7f9f6136c4897cd041e6d0e9c0e6b2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9bc3135a81faa9aadc6051ad8a251414.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9c482f8a39b9a17c7a449e44da79b7fa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9cd896240957523db4ce66679ef5d99c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9d208c63aa12be12c34b7cd2fa13c1c1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "SCIENCE EXHIBITION @ MONTESSORI",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9d40507a3c55064678aa5745155e46ba.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9d6122db625a462ad69a3a1f91901ada.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9d67263eceeb08286a029d828d814e95.webp",
    "context": {
      "refs": [
        {
          "alt": "FEEL WITH YOUR FEET - VJM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9d959dd639c49a06d818aa7d47f99709.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9d9bdaaa774728aa2c478e3cb89a0f3e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9da63c9f8d87bcfcc91130bab0015c24.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9e2c009fcbe7e57e0a495bd470f2dd6d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9e5fc004b6bae42b13b517ea83666931.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9e9df3cf76699b8ada19f6369412ac78.webp",
    "context": {
      "refs": [
        {
          "alt": "INDEPENDENCE DAY",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9ed427fd5fc07c5522c03a81fc6d327b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9f1c1ec42ce41b11edb7fca40be84aad.webp",
    "context": {
      "refs": [
        {
          "alt": "DINING",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9fa5f9cd6e87dba9680c69adb8256cb6.webp",
    "context": {
      "refs": [
        {
          "alt": "Taluk level Vijnana Bindu \u00a0(Maths workshop) \u00a0 Vishwajyothi International Public \u00a0School has won the ",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9fda7db03cc1b79dd760ad2c53e686e1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "DEEPAVALI CELEBRATION MONTESSORI",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a01cf3a86b1488915f5f51e62d1b5fef.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a069994d9b84d072d17b3593f477245a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a07c4d53bb1fe634a246183cf470aa84.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a098b88d40ee18f5f113f3716c4afec5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a0b1a0e14c7208ff2bd8ad249f22c623.webp",
    "context": {
      "refs": [
        {
          "alt": "DSC",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a0d273321f2e89cf9bfdbfa9f1ecb781.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a0e40154ca0e71fb93791c48c9d495ba.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a12e241debf9627f9e20a0f8fc4b686e.webp",
    "context": {
      "refs": [
        {
          "alt": "COLLEGE ORIENTATION DAY 2016-17",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a19147df87582e0d29e9cf76bca69fb1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a1d2bbc61b8f59b7c73e10432f28cf4a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a1fd4fd0ee00a3c1ed00762d400744d5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a2087a3db3880edea383f2a440cb9138.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a20a7c54f36f6a66c622be58f744545a.webp",
    "context": {
      "refs": [
        {
          "alt": "OTHER ACTIVITIES",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a2109b48bd2e64846b654e16d7b57664.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a22892623202ab36b96797952964aa93.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a22d95ae183271e5ae44251ff4d5ed53.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a24e3b238906730dda901cc5320e992f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a25c5c7c472035694dde9eff2bba9bf0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a27fcc1758d11051f0f3f46f9121a6c1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a2cf879e04d89b709225b24dad78d504.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a30e7aec632c11cac1912df22fd2e72b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a3cfcdbf26ec51348584d74efa8b8f2b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a4c125087e87c920e7eb69a533ce5d45.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a4d12d9c4db88fc4ea498632014a3173.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a4f16ecd5aac144eafb9dd8d7201a68d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a50a4767831385e01b4025a3acbc40b4.webp",
    "context": {
      "refs": [
        {
          "alt": "Kannada Rajyotsava Celebration @ VIPS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a51e2333ec4e8a4969b6b2a9170fa4bc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a530e389a5033e8a689921169496b8e7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a538959124510127a193dc9465ffba22.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a56d200d988b760e07d9bc8f8fe76d5a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a5a58a8bf9337fb9e3ef067d4d63115f.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a615eab66dc232364e6583ad0df9f867.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a618c1f17c5c6620eb7dd9a1831ebd62.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a658ecadd867548dd1530007a3102633.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a692d87b7e07aa0dc3891ddbf7e56e1a.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a747d8b98857d3a42b04e035606b8e90.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a795bee0c3cb8ec91d0bab24fab7675c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a79604a80c6df7bb194845e82cb3e60d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a7c5441a592a90e4bae73d1b0f70640c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a82cbe89210f0fc879b0f2e338dc97d4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a832a8664be5e08af15dd2778c9bac56.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a838377cac6324ebff9cae9e61bd4a65.webp",
    "context": {
      "refs": [
        {
          "alt": "8th ANNUAL DAY CELEBRATION 2016-17 -",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a84cfc65bc35c33390e50749f5227aeb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "%3Cstrong%3EANNUAL%20SPORTS%20MEET%3C%2Fstrong%3E",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a87bc69d937460d8b13849d925eeade3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a8a4b5bc7dcbf10288bbd09f8f421809.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a8b18b777796097a4ea58282da86fdaf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a8b8f7244d48a46e68d5343b300d7c12.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a8c8290af204e2cf10fff715bf6279b7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a9285ab5e09811337397e83fa3583e8c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a9478c368efb18d7eb38c6d1d3ad314b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a998a6e9644165a51829eb384c5203e8.webp",
    "context": {
      "refs": [
        {
          "alt": "ADVENTURE CAMP 2016-17 Mr.Jyothi Raj",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a9ea9d21f7e876f1f89a527c4aedf175.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/aa2354e169e8d50b2623965cb893314f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/aa8b30642db7f23d01e04a27fdb37f1c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/aad774e9740736ab123fb57c2ee2ee0d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ab8a8be0037346ccc575d42f6c20b460.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/abdb07935c879cb8e3335e3c7d4d30e6.webp",
    "context": {
      "refs": [
        {
          "alt": "VISHWAJYOTHI MONTESSORI - FIELD TRIP 2017",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ac00a71e8db37461ab1f5307f79a6174.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ac190c1beddc1186b49e1d54d6d433fc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ac6976ff730ab3a9eebcdab7dc4fc89c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ac6aa072b99eb34a2f7cd6828bf65ab0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ad05550528d6c5bb7def38ac42cbcbb7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Christmas Celebration",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ad3447a5e2ee5f9f6f9031cef6bc071c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/adba9f245db37a35d25eb993effef7ca.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/adbef674f786dbaf754c4f738305dba2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/add59348d22adf584ab93105c3812206.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ae5daa658b74950918396d56e0ae38c1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ae5e9a771d6e56195da6f145ce487a03.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ae654407d393ce32976ef7f5ae4fc5c2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ae68adf16383bd11706e88cc8dc9dc1b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/aed1737a804ff816f49196150ea2a65d.webp",
    "context": {
      "refs": [
        {
          "alt": "OTHER ACTIVITIES 2016-17",
          "title": ""
        },
        {
          "alt": "IMG9405",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/af07246bd14ed7ff2491448f209cb57f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/af1012762600e027441bf06cf11f9fc0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/af1033066ac612d21b9c02e13027444f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "REPUBLIC DAY 2017",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/af3848182a3d499e098382c06b6587d6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/af3f3fdb570f82b6ff6a77c0ce613e29.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/af40cb2491d255cc242099493ac04c81.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/af54966e301374c1c05277d732215e43.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b02fa8fe5acb6bcbee4d4ec17fef3b3f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b06986d93f1b9b768a9b87b7da87cb5d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b079e5bf8c9cf896e8e4542072c89def.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0ca83d77c9e4a566e1caa605ecab194.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0d8a52af9705875479716cc31092feb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0faf62e283b9c9303506897878f57d9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b1360725110b77dce66e7531f5960aa0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b150e89108d086d7bedb6df41b3c2c07.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b19616aef37bf26f138fccad45ea324d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b1c754e07d0984b20017e02a52847b31.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b1d53d10473a5a7406fa5bd4869411f4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b1e143827c5b487c10ffbd1a7480ea40.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b1f53d9c099b84db5548b7f4c7e12ad5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b20647cfb7a0173cc265127b526a302f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b216e8ed373b98072ff0e617d68e2762.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b220820cee9fd494ba11e42f98daff3b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b24c7e1707370e12e31ab3c1aa2cda07.webp",
    "context": {
      "refs": [
        {
          "alt": "Taluk level Vijnana Bindu Programme (Maths workshop)",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b256af0b882d8d8c696b83785239c96d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b258f0e59d178deb32b028f6ba0d7ef7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b267536f93bdf21eb7b1aba210e70acb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b27c4c20d1278c6ef790fe5f4e94dd7c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b284f4a6caa1210024625ee2ccc3f3d6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b297213bc080d0ae9ee0ded67dad0cc0.webp",
    "context": {
      "refs": [
        {
          "alt": "INTRODUCTION",
          "title": ""
        },
        {
          "alt": "Montessori",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b30437d2b567eedba752b261adc25543.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "CHILDREN'S DAY CELEBRATION @ VISHWAJYOTHI MONTESSORI",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b3c35eb52abb3e320f7a4118156a9325.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b3cc2f8246d1b3045e87561f83278dad.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b424b60c5a35e8dfc71f962d1139b2de.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b42f6ceb773dc61015a4adfa772bd653.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b43f4d7f1cf96016e223c0861abb43a5.webp",
    "context": {
      "refs": [
        {
          "alt": "III Graduation Day",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b4f170fc7172c06efc06af4353da99c5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b5865adaad5d73cd6148f5daf2a6fcf0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b5bbb3ec6156f2b656fdfda0d105a330.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b5e9d665041b8d94eaf193da80221c1c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b64c9fabff32fe330eaa86467378e563.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b6fa47215272b4b625274aebee8c8624.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "NAVY DAY",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b6fc5fcfaa2864c064102e0daa80db06.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b70fd5801ca1f566e6b87e6804484d5f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b7271342e1db38f4f3ee428d996fc125.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b74612bd52de0a0fadc650348152cccd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b74d06479fda726204c7a37413e69694.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b7890c5a22fe1dfd96e2f6cee4d694ea.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b78c914690475dcd10e83808da9f6428.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b832fa2a86475160c8d1bd3fbf4b80ab.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b8959a2078e1deb90487fe56849fc485.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "EXHIBITION",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b8c93db1b163f0b5d669f978a59541b0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b91f358f751312e653798a27b8a6e244.webp",
    "context": {
      "refs": [
        {
          "alt": "VIPS Latest News",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b95c1dd94d4bdafa8409c4875133af8d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b9d1204c7879b666d672e8dd84b52654.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b9f58f227dfb9dbdd4a2cc64f915fb3f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ba06aa5f024086c793ebfc108de22256.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ba10e237f32ff43c68c034d5441267c1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ba551c2820ea665eae1d794510e261c6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ba5bb93573ae9bdf55b11d99cdc87bb8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ba6b9f3c6022f6cb7d8cfd1b554cd2bf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bad0971dfc72621bb9e7381cf0671bdc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/badd4f0631f4ff84131d07e372c192bf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bae9e532565f000edcafd514e25fa683.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bb1e7a84fc7432d412d9519a753a38d1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bb305cf44d16d04a1cc6f9098858a2c8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bb6943c9264a3ddf98269023a16f2481.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bb98ecd0cc6fffe15ebf89d65052bd0e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bbd0b436d15efd1b6fc2925440097bd7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bbe6f983f0495f520604abff8e9192b0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bc09e60c3f52e415052b93f9e29092eb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bc27de4ac04f75063dd48b2d694ec745.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bc4ce9f3f7c43fc387e00df8a7e89670.webp",
    "context": {
      "refs": [
        {
          "alt": "FOR BOYS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bc539263224cf1905f3833575a644ac4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bc5fc0cce6c5ebcc2a8934bb5b4566be.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bcabcb46a9c7a3d9f752af96c4704a70.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bcbae89bcf0972b67c5a075631918ece.webp",
    "context": {
      "refs": [
        {
          "alt": "DSCresize",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bcd33060f5e8b28d8ef0b844c754e6ee.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bcf59b1434609219328f6b52e1e3fbaa.webp",
    "context": {
      "refs": [
        {
          "alt": "Story Telling & Circle Time Activity",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bd2e1cfab6c5ceb9e2f43534864310a0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bd56256eb61a1c9415dbb7b8c7491f64.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bdbbbf7267bfa6de75839a9a2221ad7a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bdf963d3bfe501a06110fb1d3871aefd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bdfdb2ea94a3ac79094024d51ed0cde6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/be64383cd1fb67d64ced7a31534d8c9c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/be735b3a7bdf21956827fe857ab63b37.webp",
    "context": {
      "refs": [
        {
          "alt": "DiningHall",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bea556280c314e4b6f9685bb52fdafe0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/befe40ed8bba2dc3bb46ac625336daf4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bf1983a3c7d569fb5982583d1a0cb426.webp",
    "context": {
      "refs": [
        {
          "alt": "Independence Day 2016",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bf256ae6f69183b3e0ac715f483f943d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bf59dc60c57fbca2e567f3b9a2645d25.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bf8afb44c8ae3cedef46de05170a1bf0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c022c27eed3a275afa0d464371d62fc3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c032ba0b948425755fdd00c3f11e7c02.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c094055bfeb0b5641a9b60f9d97bbbc4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c0e666f4a76a2f7310dc98f689fed80d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c1066953b8bbe22bf9a8528c11c39845.webp",
    "context": {
      "refs": [
        {
          "alt": "DiningHall",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c10f01cc0d997e687c5ba0dfaca03ceb.webp",
    "context": {
      "refs": [
        {
          "alt": "PARENT ORIENTATION PROGRAMME",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c14a5fabf38e2e7b81891e40e533f6b8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c16c7d6b1d6f98e652acad628db51e21.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c1a7922feb74be76503d93bf16e1b500.webp",
    "context": {
      "refs": [
        {
          "alt": "CURRICULUM/TIMINGS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c1aa13d2cd82e6d9cfda5ecc8f1e82b2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c1e376f6790933473bf3b0add348cf14.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c1e3a2530d272f5d92f3a9cc79f20292.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c2c26237bda7a2dcc535f7b2942bf32e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c3ecfe16f502f5e9e677bd08ef94f9af.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c4445eced18b75d05f8bc451e4d7fee9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c452ea65c3106db2fb273f1659f745a4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c4ccbacd69b663d5e20ac1eafc2df80a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c4f828603857bc35bfde096f23527a01.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c4fe2e16930a86d05310984ea41815b5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c521aa933f5aab4ac6671d6c8686f0d9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c53123b34d0c313f7942e1ab0c45bd27.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c55dfff83606f201f286c1f73e365f8f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "IMG",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c56883eb925534fb72b5d5395b3f108b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c58fbf85388f977782d76b55f44fba11.webp",
    "context": {
      "refs": [
        {
          "alt": "Logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c5aff4ead4ebe79f4761d4f88330705b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c643449c4ab9eae901492e5fcaf8cd9c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c65e9183ff3b6940c539da4e2aa6ecc4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c6a136daa40b68c3bb88c5c9b437d382.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c6e8c8cffe0d659c618d810f0faebaaa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c6edffba77d82aeaa36ef0d74eda00d1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c788a5e40da9c6e69cb89ef2c0056e87.webp",
    "context": {
      "refs": [
        {
          "alt": "DiningHall",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c7c9095aac8e6fc29638eafafaeb71d9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c80e2f48832dd4b75cd60199c8e7de84.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/c8444eef9ad139bd4481da5e3efedbdd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c87dd04a1327a16b2855cfe4f4564f99.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c889448784d899cac920bd49248de4f7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c89eb68c3990ca3b982b17317aded9d2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c8dfd76b1d790b55732e5801579a47b7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c9dfb9cd601531bb8854cadb1591144f.webp",
    "context": {
      "refs": [
        {
          "alt": "DiningHall",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c9ec3fcc8000102b3e811366f6181754.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c9f16ec188c7511e4ce6e58287ad6781.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ca1d0b937b340a2ceffd67656fd76caf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ca348e520350cb5dac5f530c1f8305fd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ca50bd5c0b7c7ba28021c6d95fc2bbd6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ca5332cd16497bc7bfa329c63a7b36ae.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ca7c5c14212130c199c7fccfb6752864.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cab2a4e6cb9e27f0d0383728c1c697f7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cb48c398d5ff2ad66ced8b4bc01f49d0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cb8074aaa465b16e35938a49271993dd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cbbdb985b35d2689c8272c797d89bc90.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cc4197c52306aa813fc756ad6eca11c3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cce222bf3612815e4f7d0c70ae5ae7c6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Boys are not permitted to:",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cd1ead1c65e1f6397a4eb89b4b1fcb62.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cd32eb4d53279f62dc23ec03b9ce3082.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "II GRADUATION DAY 2016-17",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cda89a77acda89bb3276a2a8702a197d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cdc1855c692a1db8d9d1c974e7a742f8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cdf9195fd5a859d1b0662ab514ccd378.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ce099fdee27c18b5f998211fabea140a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ce1591bcba319856c54820fb23ba3862.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ce438dd029af398c492262e347d17039.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ce824141f5c6984e42c1f2359e1f714e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ce9e981fb7fd3ef394ea1b1ce9078b6b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cefec60922bfed1161ea00583e5e09ef.webp",
    "context": {
      "refs": [
        {
          "alt": "4th Graduation Day of Vishwajyothi PU College",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cf30acf7ed020da749399a7c15f46189.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cf4451952f7202c72cc857f73dc8afd6.webp",
    "context": {
      "refs": [
        {
          "alt": "CALENDAR OF EVENTS 2019-20",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cf5dee1be14855ff6f203e3f07458048.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cf5ee7ab690b7eaa8845b6349925811d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cf750e5a307d3db74f7646854a697f8c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cfabbcda63527ca3e2f338689c0aff9a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cfb4a1a3e823d7189e6b6640fcff7de1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cfca2298935a6bc1d3b05351116fd92c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cfe12747a761bb66523b19b5420a9f47.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d073f42d8a0b58c9e5e81cbcda2dc59c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d0ad8179b50b4a448a97a7025f2dfdba.webp",
    "context": {
      "refs": [
        {
          "alt": "PHYSICS LAB",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d0f61eec359f79b46869c2ac89d9a8d0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d13f026b51e3de71053d7276c062db69.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d16e33c51e8b56df9861d1d9e2d3fbe2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d16eb98ba5b6fbad79d66f80949ddba8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d19a96ec767065b1f2cadcafeee571b5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d1c430e447f8fd491d2dba050f395eea.webp",
    "context": {
      "refs": [
        {
          "alt": "College",
          "title": ""
        },
        {
          "alt": "INTRODUCTION",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d1c8494ffb817b88a88852cf1b125859.webp",
    "context": {
      "refs": [
        {
          "alt": "School",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d205f2ce63899e1477afaa8145abb7c1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d24ab8e0c275479cca6c2676336a310b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d24e4c0dd8caee19a79824446b894885.webp",
    "context": {
      "refs": [
        {
          "alt": "8th Annual Sports Meet (1st Day)",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d2ffdde7c117b2350ef50713dd2a2a62.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d3109153318222d3eece416e1a3b926a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "IMG2152",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d331fc0638d4943a03cc7344a1c61768.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d3580f05464e4089d42acea3b90d1994.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d3789f4687d4ad5f514787da2b4a70c4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d3b9fc8048ff09e9d5e158052b4d09fb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "IMG8588",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d3ef6bf95a13c879e56cf64596ec189b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d43586d4d794268e94623ca8fd0e2ca9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d43e72e9e8340b04314a03247f04ba4a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d4542458eb1526c569ac0ebdb8198b93.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d4b87baa6f29cd0d1f7997d83cc72fc2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d4ea197b7444175a14213cb91e567a9e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d50eb4ccbb9e3ee40b0e056f6915a4c0.webp",
    "context": {
      "refs": [
        {
          "alt": "ANNUAL SPORTS MEET 2016-17",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d525b7aff2213cd1cd473bafcaf98bad.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d544c5c6927c5e33cc9dac16e23b54f3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d595e41e7e39c4ef5333fadb95d8f78e.webp",
    "context": {
      "refs": [
        {
          "alt": "ENVIRONMENT DAY",
          "title": ""
        },
        {
          "alt": "IMG4656",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d673bc7229e95923461bce3f8fb683bc.webp",
    "context": {
      "refs": [
        {
          "alt": "Independence Day Celebration 2018",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d6c51241d1831427bc7440f8b7290da6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d6e1c14961a22e034bf82be4a69fb0fb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d70d8ed33a3394ed2db06ecd34c98e82.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d70db79d95d1de3df42a5085fa346f04.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d70e64759bae8b7df36fa8a585bc4899.webp",
    "context": {
      "refs": [
        {
          "alt": "Red Day Celebration @ Vishwajyothi Montessori",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d730d6e32b60a5ea86daa929a3a3c7cc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d7393f77c53b4159b25ab848179a10c2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d73c59adbda0bbfbc0f999389667b189.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d83cefeadedb5c27e142fe5bd8e1a958.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d85827d29b87598e050bb039056159b4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d859556f0908ed8780a0c5ec6b10eac7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d8b3f274c88ad5714dd9d513ee3c68a9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d8c63e7753afab4ef97ee1eaa7a6f6fa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d8ceda2c86f3cd2f10747889352cc1ea.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d92a202e38da5dc0454818c63bb026a8.webp",
    "context": {
      "refs": [
        {
          "alt": "Orange Day Celebration in Montessori",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d95d16d0658e5063361fb9ea9fd587b7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d96455aa095db8b174101ce9efb476e3.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG9817",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d978c244c445a174ffb7f3075b00549a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d9f230bdd4233a470c9c2ab494a058a4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/da11975deeb46b80b31649721a72726f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/da1f66ce5142c46366dbe0c7e7692b84.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dae80a809937a8daeb7e38dd49cb04f2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/daf579557614660d72b72d280ec78f35.webp",
    "context": {
      "refs": [
        {
          "alt": "VIPS Achievments",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/db168395ac031eff54be2cd1cb17f52c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "IMG",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/db39cbc9276238a592c3d8a88541d16c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/db7cbb9ecb4fdc5196ba7d54eeae3e48.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/db917b7af108d764689251688216336f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dbae6c3b27dea093ca8720d72fc9e8b4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dbe9d6352d78a757ff18ddaa96f1ddd7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dc1b6a777305ec24c7ae621afcb3f7ca.webp",
    "context": {
      "refs": [
        {
          "alt": "DiningHall",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dc587269e692ef48b3ac0a9cd18a6324.webp",
    "context": {
      "refs": [
        {
          "alt": "RAMZAN CELEBRATION",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dcce7301b4351e5951cc0e8500496af1.webp",
    "context": {
      "refs": [
        {
          "alt": "SCHOOL CAMPUS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dcecdf01dcbe80a49c5b694e8753c406.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dd55ece75347bf665198ab5d332d9f04.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/de1a13f5a9b39659e49df8b729d98199.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/de49345069ed081175758cf74c1f113e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/de68f7ec037d447b584cdd9e4524ab18.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/deeb18e08d2e92a263a5f8d6a69f46e5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/deeb8bb689959821669383b950357efb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "VJM RAKSHA BANDAN 2016 -17",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/df5d579e8290bb84b9f6838cd7744168.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dfa80296b846d53f36eef61835f42cd5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dfec47b4b7aee15d31398813fa7f2080.webp",
    "context": {
      "refs": [
        {
          "alt": "PRATHIBAKARANJI TALUQ LEVEL & DISTRICT LEVEL WINNERS 2016",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e0909b72a7efc9244492a58fbda04d96.webp",
    "context": {
      "refs": [
        {
          "alt": "Sri Krishna Janmastami Celebration @ VJM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e0de3a24586682bd284bb6594bed7225.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e10005a0eea20d16cfea32ba86056917.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e14199c312b8355dd1a58f068966a811.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e15c1f45cd8f1e334f638dfa7881a127.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "ANNUAL SPORTS MEET - VISHWAJYOTHI MONTESSORI",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e17ec145ae61c9726b4ffac4bcd4722b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e19078d6cabe506f04fce6856b919b35.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e1d9b750d638fde08a40527d19254ab9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e22677f4851285b52214b74c7bf350ff.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e23890e6466e101fd8fc546bba07b801.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e280f15f560e2c67b2a3fe848ca55e9f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e2a51354dd39a7aa91d0b388ab105aad.webp",
    "context": {
      "refs": [
        {
          "alt": "DiningHall",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e2a744acc86d7be4e10192c444f1d0b4.webp",
    "context": {
      "refs": [
        {
          "alt": "SHRI KRISHNA JANMASTAMI CELEBRATION AT MONTESSORI",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e2e4ced7e4a6df943048d69e0dc26a00.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e30d0001195677babb30583c1948c2b7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e350647cce427cce7eb5889c459528ca.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e36880639d8e952e55a0dfcbc52672dc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e39744a49395914cf25799d1c34d688c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e403c21bf352ef580db3f38686b16b5e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e416183ca9cf454bf4bcc5763493f756.webp",
    "context": {
      "refs": [
        {
          "alt": "International Olympic Day",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e420ee87e845c4275d6aae4a366cdfbf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e42bb5561e078944b43f36f3f30492c2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e4619dc77485aa76cc72f0e9e6d5a258.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e4890f50a9a8bf548d98c0c8bf6a7d41.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Farmers Day Celebration @ Montessori",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e4958bcb55a47703afca98dba12a2b2d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e4ed23ab6e36f07ebbcce0727286b23a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "IMG0047",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e4fd2775ec3cb8fb9dc264f9ccb02f14.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e552d854a5d492da1faa6510a5a33c72.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e5630a62a44343e8d6b084aa1e53e53a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e5850a9ccb6abd6aea4f7b013a0d2cae.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e58cd5121f46b76cead0a830f984156c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e5b8b51a94780354d1cf63ec101305ae.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e5c5cd7ceadd6981a83ebd8ae591f6b7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e5cc80e8d133e373525841f243a323d0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e61399ebc681cf9adac60dda90ebf105.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e660f9c52d0d2b12af83de2c695907b6.webp",
    "context": {
      "refs": [
        {
          "alt": "Sri Krishna Janmastami Celebration @ VIPS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e6860bf49c5a824ac25b06e52c01078b.webp",
    "context": {
      "refs": [
        {
          "alt": "DiningHall",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e690aa760798f5553f73611ab9dba621.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e6ab36a6026a2af9e5c0d584d3929218.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e6d756de37c4defb958eec225b3add2c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e6dd2e7f006d69875bf09896994c4f24.webp",
    "context": {
      "refs": [
        {
          "alt": "Decennial Annual Day Celebration",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e8166f12f4abff63b20a895aa212383b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e82fc778e5ba57b8cc5425d555311548.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e84491aed63e412f78d5b0c7ade3ee7c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e890a9ff0d84aeddfb771cd24b2fcd7a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e891c79588951f003698f61e4e296144.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e8d0dff36e75d8cefaa061b77da83bf0.webp",
    "context": {
      "refs": [
        {
          "alt": "VISHWAJYOTHI HOSTEL INAUGURATION CEREMONY 2016",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e8d270f82b7d77142cceb0d75043ae94.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e8ed8b1705396074e2a96ca7bcfe7229.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e93db154584eb00c9689653e2576029c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e94df49558405fe351bfb0edcc16c0cb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e94e9977023ec6df36759a296e5ea821.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e977de572acdfc50e5d27bb6eccd5c3e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e9857d3fea28a3549575dc6cbd148503.webp",
    "context": {
      "refs": [
        {
          "alt": "DiningHall",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e9d86b432da9f1f714bf18998ffafea3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eaf6162fd60ce3379d103851e06dd35b.webp",
    "context": {
      "refs": [
        {
          "alt": "COLLEGE CHILDRENS DAY",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eaf93189671805a619a1e9d1b774f618.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eb039ceb760eb8ff082bb5627dff4299.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eb3a8c73b535f283b642ae59fe02c0e3.webp",
    "context": {
      "refs": [
        {
          "alt": "INDEPENDENCE DAY CELEBRATION IN VJM 2018",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eb58a2d273c57823ca10c37667f73080.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eb5f765918d8ba2f88432201dac64c99.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eb68caddf0f962a58ff42a87b08781d7.webp",
    "context": {
      "refs": [
        {
          "alt": "DiningHall",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eb7d266989af409bdd156fd682d9edc0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eb8613e5ed2837794235937b73ac312f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ebbc7afd8ae8e274d0fd703186060b99.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ebf957ae8d020fd063f5c39ae160c521.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ec24c466ce86a2d5795093f5122a394d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ec86f9f2f5910210bfe04a72772d9317.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eca0fcea4e4e30a6d128c4e0f9e65e7c.webp",
    "context": {
      "refs": [
        {
          "alt": "TEACHERS DAY",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "IMG1810",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ece473cf428421bf7889f569eee1cfe0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ece48f35febb0d601dcb6fe140915c4d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ed43f12a5944ec39351baf0ab8ee8fdd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ed501f2b7755a378010496737284cd28.webp",
    "context": {
      "refs": [
        {
          "alt": "Logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ed560fd35ccc0a6cc783a8b36757d230.webp",
    "context": {
      "refs": [
        {
          "alt": "2nd Day of Annual Sports Meet & Prize Distribution",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ed86653fe49c31d1aed82fecc8c6537b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eda5d612c6521a890df7781974eae9d3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/edb9aee9f7dd44ec2434e6005391ab58.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/edbc8b6b0545bde646dcded2dce5ea51.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG4656",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/edca964d05c34cbaf58adcfafe0e8fb2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eddd975f484f933b250b6970b09fc301.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ee9a37a763dbf97ac22afb320d6ffa47.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eea0a5312b2ac20878a4a54e9ee62645.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eec658476a636e2ac80c88d7ca5d89da.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ef03dc315abd3c9af5d9981dc8fb9972.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ef1c0e0a12cb94f1d92d001aa60081d2.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ef9bace231f017867ec453ce5cf0ba8f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/efb942566638aa95542cc2cd1b9287fd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/efcf3283c161cec5fa8f7428da490cf4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/efd382c225ba4b9041764b2fdc254abe.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/effd04c4fbc68d3458285da971e3ba7d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f005eedeeb4900fcba33bbd4a8b689b9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f0163b167c04b0918e701b65e6092f61.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f022b3d431433148ced2f7b45af89c64.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f0c002ed05bf961a682151b028557415.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f0cceecaa30ead98f20794641d265c69.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f0ce658d370a778815fc2f46bf738c2f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f0d3670c07b7a028ae5474665cb5b998.webp",
    "context": {
      "refs": [
        {
          "alt": "VIPS SCHOOL TIMINGS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f10d838d582eed05e1a354f70dbc7497.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f1b54d2bd95d25f8052b8ea1c6c2f122.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f20b7e2c9ad80fdbf846ce57b5c1774e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f20edb56016351b9c3d7f284fa232a3c.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG9817",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f283a0a266b3c0af1eb89da2ff2d2f99.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f2ce7b6efbbab98a6d4ea6459feebacd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f33a690eb3757573a187d228bf99b61d.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG0489",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f3544e2d09010781fe1ff057c62925d8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f3e2d24195828b70d33e6f16a27f2d75.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f4107ea4aedf3d66f8df4b25b39fb8a3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f472ad14b2c854754dd9927d4b48f0c8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f4cda0a53ef87e4be7389ca9c3a1ad2c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f50ac746f4b2ea82f27174fdff75869c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f5179404f6d7aad3237f81128036c452.webp",
    "context": {
      "refs": [
        {
          "alt": "DiningHall",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f549399790ce18f3a6f398d36d73af81.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f5ac1082df0bda4f6d04fc4f4fb7335f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f5b489c8fc9d61ef228e0fc48915ddf8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f5d151b5ff59a44e87668935c2862e6d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f5ffda8e2ff97400b55e8c921d058d43.webp",
    "context": {
      "refs": [
        {
          "alt": "KANNADA NUDI SOBAGU @ VIPS",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f64dcd1c216252e0acba3199a3845919.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f661d8400cb29e48dbd2ea2de1b5fc1b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f6699fb4cb7716f6ec6353075a20418f.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f680d3e4da617cb2eeef3e02d0fd7a0d.webp",
    "context": {
      "refs": [
        {
          "alt": "REPUBLIC DAY CELEBRATION 2018",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f684b70ab6f91eebab83b35e734dfda9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f68e7aee8387f3e78d82ad6399c768e4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f703a418e06083b8bc59b836cdcbb70f.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f70f512c2ad2957b532ebe412d0046bb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f71902bfabbdf5c541436956f6b0ba04.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f7773147bd0b2b3ba6c1827cab01923c.webp",
    "context": {
      "refs": [
        {
          "alt": "DSC",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f787afae97aabe1cec6dcbbe9da2dd1a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f8615f115f1de0373b141c3cbeff99c7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f87831d08744ae6807aec4d34006f483.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f890944c811ae16031bec0300fcb078e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f8b170e349b8adc61614589efc281ec7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f8dfeeb8ff092272020fe009a53bcea8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f916ba6aa1217d3dbb63209567a1fd67.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f96de61eb1052aebf84d08addb8ab1e6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f98dc1b56ef44a9ddebdc80252b72f9d.webp",
    "context": {
      "refs": [
        {
          "alt": "FLOOD RELEIF FUND CONTRIBUTION TO KODAGU FROM VIPS",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f99bc9ba9247910c2af576fe60b940cd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f9e5910dac00feeb1f77052d4a3a6a1a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fa0f85059585fb4b2fc53e54f8365d71.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fa5210780f79604e5472fa62b6ba69e3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fa8752bb49115d474d3ed643edc0186d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fa9abe8ccbfe630af62141ab09dbca8a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fa9d8f0510dc7bf76c9b5ee324c2630d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fad4e4ecbb72061ed3ba2c3d8da73c54.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fad9e7d73441c6d2c9ef61fff9536602.webp",
    "context": {
      "refs": [
        {
          "alt": "Celebration of Dasara in VJM & VIPS",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fada607c140f112a25d60442a83c2507.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/faeffc5b535cfa58a2369be7ded126d2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/faf0c42293f9e34b5c4a45952e49c8a1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fb0f493ac422da08764c4d096afefed3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fb7d577828b6605f1827df1017d981c0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fb9751cdf1757fa613aa72949c3c3cc4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fb9dac71fba59d879384859f04f0cf22.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fbb07e60dea66b58bc8f22d8c22dfeb8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fbd70103357992b4682ef581c3fe6c24.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fbebfc6c97b99d71af51690f89e7f4d1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fbee22924ca1d3b17dd11c3cc4fddffb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fc6c29e7f47c62e15cbb3cb5e79660e4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fc766bc84b3aeeb4d7095913ed8c4461.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fc8f4b73f4e56de68d6e7eb082103994.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fcc13a3aa6451b8edb586c36aea51c23.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fccf6c0eb6d818dd770fe68fcc322953.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fcef728276967a806ee1766c8e598862.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fcfeca4c1bc65a5260810b805b7cc9f4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fd451456f5236963479ce038fe27874d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fd4882f2ffb5f0b325600dc85114cb02.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fd49b743fe0a923552c478907de1ed30.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fd8b7b8286ed872153973c683063f63c.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fde5e942cd2f192610ea9e91da5e7baa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fe1a0413f3306ee05b92071f799797cd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fe1e24450a3076170c818d839a5b815f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fe7489e1cef7fe3e5c476dca41949320.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fe7fbd207cb30f670af264e4c78fe6f9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fe9a8ed6719ca557975c84c676b53c6d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fecae7254ed23b5d7ba0e1838d5b0627.webp",
    "context": {
      "refs": [
        {
          "alt": "Share & Care by Vishwajyothians",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ff946ace6229a3b6e2e51d616985bd61.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ffb7bc413de378b9fe127b2195387476.webp",
    "context": {
      "refs": [
        {
          "alt": "ADMIN STAFF:",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ffdd8c8e07cbcfb7bbac7393b15b9b4c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "VISHWAJYOTHI INTERNATIONAL PUBLIC SCHOOL | BALLARI SCHOOL | CONVENT | VIPS | VIP EDUCATIONAL TRUST",
      "first_heading": "WELCOME"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  },
  {
    "path": "latestUpdates.html",
    "context": {
      "title": "LATEST UPDATES",
      "first_heading": "LATEST UPDATES"
    }
  },
  {
    "path": "test.html",
    "context": {
      "title": "",
      "first_heading": ""
    }
  },
  {
    "path": "vision.html",
    "context": {
      "title": "MOTTO | VISION",
      "first_heading": "MOTTO &\u00a0VISION"
    }
  },
  {
    "path": "vjm-school-openind-day-2018-19.html",
    "context": {
      "title": "",
      "first_heading": "VISHWAJYOTHI MONTESSORI SCHOOL RE-OPENING FOR THE ACADEMIC YEAR 2018-19"
    }
  },
  {
    "path": "www.vianabus.com.html",
    "context": {
      "title": "VISHWAJYOTHI INTERNATIONAL PUBLIC SCHOOL | BALLARI SCHOOL | CONVENT | VIPS | VIP EDUCATIONAL TRUST",
      "first_heading": ""
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.