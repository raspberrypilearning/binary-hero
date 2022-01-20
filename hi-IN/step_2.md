## कुंजी दबाना

आप चार कुंजियों के साथ कितनी टिप्पणियाँ बजा सकते हैं? आप जो सोचते हैं यह उससे अधिक हो सकता है!

--- task ---

'बाइनरी हीरो' स्क्रैच स्टार्टर प्रोजेक्ट खोलें।

**Online:** : स्टार्टर प्रोजेक्ट खोलें [rpf.io/binary-hero-on](https://rpf.io/binary-hero-on){:target="_blank"}. यदि आपके पास एक स्क्रैच खाता है, तो आप यहाँ पर क्लिक कर सकते हैं **Remix**परियोजना की एक प्रति सहेजने के लिए ऊपरी दाएँ हाथ के कोने में।

**Offline:** ऑफ़लाइन संपादक में खोलो [starter project](https://rpf.io/p/hi-IN/binary-hero-go){:target="_blank"} । यदि आपको स्क्रैच ऑफ़लाइन संपादक को डाउनलोड और इंस्टॉल करने की आवश्यकता है, तो आप इसे पा सकते हैं [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

--- /task ---

कौन से कुंजी को दबया जा राह है, वह दिखाकर शुरू करें।

--- task ---

स्प्राइट पर क्लिक करें जिसे '1' कहा जाता है, और स्प्राइट की पोशाक को बदलने के लिए, कोड जोड़ने के लिय `v` कुंजी को दबाइए

![पोशाक](images/1.png)

```blocks3
when flag clicked
forever
if < key (v v) pressed?> then
switch costume to (on v)
else
switch costume to (off v)
end
```

जब आप अपने कोड <kbd>v</kbd> को दबाकर परीक्षण करते हैं, तो यह स्प्राइट ज्वाला होना चाहिए।

![v कुंजी का परीक्षण](images/1-test.png)

--- /task ---

--- task ---

अन्य तीन स्प्राइट्स के लिए भी ऐसा ही करें ताकि अगर वह प्रकाश करें ज़ब keys <kbd>z</kbd>, <kbd>x</kbd>, or <kbd>c</kbd> को दबया जायगा

![सभी कुंजी दबाया गया](images/all-key-presses.png)

--- /task ---
