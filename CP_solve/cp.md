Markdown
```cpp
১ থেকে N পর্যন্ত সব সংখ্যার যোগফল formula
total = N * (N + 1) / 2;

১ থেকে N এর মধ্যে শুধু (Even) সংখ্যার যোগফল
C++
even_count = N / 2;
even_sum = even_count * (even_count + 1);

১ থেকে N এর মধ্যে শুধু (Odd) সংখ্যার যোগফল
C++
odd_count = (N + 1) / 2;
odd_sum = odd_count * odd_count;

১ থেকে N পর্যন্ত সব সংখ্যার (Squares) যোগফল
C++
sum = N * (N + 1) * (2 * N + 1) / 6;

১ থেকে N পর্যন্ত সব "বিজোড় সংখ্যার বর্গের" যোগফল
নোট: N যদি বিজোড় সংখ্যা (ধারার শেষ সংখ্যা) হয়, তবে সূত্র:

C++
sum = N * (N + 1) * (N + 2) / 6;

১ থেকে N পর্যন্ত সব "জোড় সংখ্যার বর্গের" যোগফল
নোট: N যদি জোড় সংখ্যা (ধারার শেষ সংখ্যা) হয়, তবে সূত্র:

C++
sum = N * (N + 1) * (N + 2) / 6;

১ থেকে N পর্যন্ত সব সংখ্যার (Cubes) যোগফল
C++
sum = pow((N * (N + 1) / 2), 2);

যেকোনো সমান্তর ধারার (Arithmetic Progression) যোগফল
C++
// পদসংখ্যা n = ((শেষ পদ - প্রথম পদ) / সাধারণ অন্তর) + 1
// sum = (n / 2) * (প্রথম পদ + শেষ পদ)

জ্যামিতিক ধারা বা গুণোত্তর প্রগতি (Geometric)
C++
sum = a * (pow(r, n) - 1) / (r - 1);  // যখন r > 1
sum = a * (1 - pow(r, n)) / (1 - r);  // যখন r < 1

Collect last digit / number
C++
last = N % 10;

Cut last digit / number
C++
N /= 10;

পিরামিড বা ট্রায়াঙ্গুলার নম্বরের যোগফল
C++
sum = N * (N + 1) * (N + 2) / 6;

C++ Useful Snippets
Float Precision Define
দশমিকের পর নির্দিষ্ট ঘর পর্যন্ত প্রিন্ট করার জন্য:
C++
cout << fixed << setprecision(2) << your_ans << endl; // ২ ঘর পর্যন্ত দেখাব

গাড়ির Fuel Consumption বের করার ফর্মুলা
১ লিটারে যত কিমি যাবে তা দিয়ে ভাগ করতে হবে। (যেমন: ১ লিটারে ১২ কিমি গেলে ১২.০ দিয়ে ভাগ হবে)। int এবং float এর মধ্যে হিসাব করার সময় সঠিক মানের জন্য .0 বা টাইপকাস্টিং ব্যবহার করতে হয়।

C++
double Liters = (Spent_Time * Average_Speed) / 12.0;
স্ট্রিংয়ের প্রতিটি ক্যারেক্টারকে সংখ্যায় রূপান্তর করে যোগ করা

ASCII ভ্যালু থেকে '0' বিয়োগ করে ক্যারেক্টারকে সংখ্যায় রূপান্তর করার লুপ:
C++
int current_sum = 0;
for (char c : S) {
    current_sum += (c - '0'); // Character to integer conversion
}

Absolute Value - abs()
নেগেটিভ সংখ্যাকে পজিটিভ করা এবং পজিটিভ সংখ্যাকে একই রাখার জন্য C++ এ abs() ব্যবহৃত হয়।
উদাহরণস্বরূপ: যদি দুটি স্কোরের ব্যবধান ৩ এর কম হলে Yes নয়তো No প্রিন্ট করতে বলা হয়:

C++
if (abs(X - Y) < 3) {
    cout << "Yes" << endl;
} else {
    cout << "No" << endl;
}

C++ এ কোনো স্ট্রিং-এর শেষ অক্ষরটি পেতে আমরা S.back() অথবা S[S.length() - 1] ব্যবহার করতে পারি।

last koita string cut korbe tar jonno
int len = S.length();
    
    // শেষ ৩টি অক্ষর কেটে এনে 'ist' এর সাথে মেলানো
    if (len >= 3 && S.substr(len - 3) == "ist")
ekane s.substr(s.size() - 3) er kaj
শব্দটি যত বড়ই হোক না কেন (যেমন: tourist, artist বা specialist), আপনি যখনই লিখবেন S.substr(len - 3), কম্পিউটার সবসময় ওই শব্দের একেবারে শেষ ৩টি অক্ষর কেটে বের করে নিয়ে আসবে।

Distance to the Next Multiple
