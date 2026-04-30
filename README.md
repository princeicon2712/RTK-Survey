# RTK-Survey

আমার সেট আপ এখনো পরীক্ষামূলক, Quectel LC29H মডিউল কমবেশি ৩৫ ডলার আর এন্টেনা ৬৫ ডলার মোট ১০০ ডলার প্রতি সেট। RTK এর জন্য ২ সেট ২০০ ডলার বা ২৫ হাজার টাকা। কিন্তু এর সাথে অন্তত দুটি মোবাইল ফোন লাগবে, ট্রাইপড, কেসিং ইত্যাদি লাগবে। মোবাইল ফোন দিয়ে বেস ষ্টেশন চালানো বাস্তবসম্মত নয়। এর জন্য ছোট সিঙ্গেল বোর্ড কম্পিউটার, পাওয়ার ও নেটওয়ার্ক লাগবে। একটি কার্যকর ব্যবস্থা উদ্ভাবনের আগে খরচের হিসাব দেয়া সম্ভব নয়।

তবে কেউ টাকা থাকলে রেডিমেড সিস্টেম সংগ্রহ করতে পারেন, মোটামুটি এন্ট্রি লেভেলের সম্পূর্ণ সেট (SingularXYZ Z1 Base Rover Kit) ২০০০ ডলারের মধ্যে।

## সবসময় কন্ট্রোল পয়েন্ট সার্ভে মোডে পয়েন্ট নিতে হবে

## singularpad   Apk [ সোহেল ভাই মনোয়ার]

## Surpad 4.2 apk [ মোবাইল দিয়েও প্রেকটিস করা যা]

## 100% $ignal 

GPS (1004, 1077)

GLONASS (1012, 1087)

Galileo (1097)

BeiDou (1127)

SBAS (1107)


<!--[profile](./RTK.jpeg)-->
<img src="RTK.jpeg" width="600"/>


<!--[profile](./bm.jpg)-->
<img src="bm.jpg" width="600"/>

## Trilateration সম্পর্কে জান্তে হবে।

# RTK command


$PQTMRESTOREPAR*13

$PQTMSAVEPAR*5A

## GNSS System Select (কোন স্যাটেলাইট ব্যবহার করবে) এই সফটওয়্যারে তুমি GNSS module-এ PMTK / PQTM কমান্ড দাও



$PQTMGNSSSELECT,1*hh   // GPS only

$PQTMGNSSSELECT,2*hh   // GLONASS

$PQTMGNSSSELECT,3*hh   // GPS+GLONASS

$PQTMGNSSSELECT,7*hh   // All (GPS+GLONASS+BeiDou+Galileo)

## RTCM Output enable (সবচেয়ে গুরুত্বপূর্ণ)

## Survey-in (Auto position)


(1) $PQTMSURVEY,1,<time>,<accuracy>*xx

(2) $PQTMSURVEY,1,300,1.0*xx

👉 মানে:
1 = Start Survey-in
300 = 300 seconds (5 min)
1.0 = 1 meter accuracy limit


## Geolocate
