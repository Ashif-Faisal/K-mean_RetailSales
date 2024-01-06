# K mean Project RetailSales

ধরি, কোনো গ্রুপ অব কোম্পানি যেমন (বসুন্ধরা গ্রুপ, যমুনা গ্রুপ, সিটি গ্রুপ, বেক্সিমকো) আমাকে as a 
data scientist or data analyst হিসেবে hire করে বললেন যে মেশিন লার্নিং apply করে উনাদের কোম্পানির টোটাল সেলস রিপোর্ট or শীটস থেকে তিন ধরণের বেস্ট কাস্টমার বের করে দিতে । যেমনঃ Diamond, Golden, Silver
Then উনারা উনাদের মতো করে সিলেক্টেড কাস্টমার গুলোকে appreciation দিবেন ।

এখন, আমাকে  মেশিন লার্নিং এপ্লাই করে এই তিন ধরণের কাস্টমার বের করার জন্য কিছু technique ফলো করে then বের করে নিতে হবে ।

এর মধ্যে একটি টেকনিক হলো RFM.

এখন প্রশ্ন হল RFM কি ?

RFM হলো Recency, Frequency and Monetary 

Recency: Recencyহলো কাস্টমার রিসেন্ট কবে কেনাকাটা করেছে সেটা।
Frequency: Frequency হলো কাস্টমার কত রেগুলার কেনাকাটা করে সেটা ।
Monetary: Monetary হলো কত টাকার কেনাকাটা করে সেটা ।

Note: RFM এর parameter আরো বেশিও হতে পারে ।

উল্লেখিত technique RFM বের করার ওয়ে :

১ম : Recency
প্রথমে প্রতিটা কাস্টমারের কেনাকাটার লাস্ট Invoice Date বের করে নিবো এবং যে Date থেকে Recency দেখতে চাই ওই Date টা সিলেক্ট করে নিবো (সেটা বর্তমান Date ও হতে পারে আবার ডাটা ওয়াইজ আগের Date ও হতে পারে )
এরপর, যে Date থেকে আমি Recency বের করবো ওই Date থেকে প্রতিটা কাস্টমারের লাস্ট Invoice Date মাইনাস করে নিবো । মাইনাস করে নিলেই যে Date থেকে Recencyদেখবো ওই Date থেকে কোন কাস্টমার Id wise কোন কাস্টমার কয় দিন আগে কেনাকাটা করেছে Date wiseসেটা বের হয়ে যাবে।
এটাই হলো Recency.

২য়: Frequency 
Frequency বের করার ওয়ে হচ্ছে, প্রতিটা কাস্টমারের id wise টোটাল invoice সংখ্যা বের করে নিবো । id wise  যার invoice সংখ্যা সব চেয়ে বেশি' হবে তার frequency ও  তত বেশি হবে ।

৩য় : Monetary 
Monetary বের করার ওয়ে হলো, সবগুলো কাস্টমারের id wise invoice গুলোর total price যোগ করে নেওয়া । অথবা unit wise sales report হলে total unit কে price দিয়ে গুন করে total price টা বের করে নেওয়া । কাস্টমার id wise যার invoice price বেশি হবে তার monetary তত বেশি হবে ।

এভাবে RFM বের করা হয় |

RFM ছিল Data preprocessing এর একটা part.

এখন, K-Mean apply করে k-mean এর centroid অনুযায়ী Diamond, Golden এবং Silver কাস্টমার বের করে নিবো ।

এই সম্পর্ণ প্রসেস টা বা প্রজেক্টটা আমার এই প্রজেক্ট এ করা আছে ।

আগামীতে এই প্রজেক্ট টা MLOps apply করে Data pipeline এর মাধ্যমে কিভাবে ডাটা গুলো  উল্লেখিত তিন ভাগে আলাদা করা যায় সেটা দেখবো, ইনশাআল্লাহ |
