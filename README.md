# Why does the external PIN pad not work with UposClientAidlInterface when launched from the Evotor Sale menu?

A question about SberUpos on the Evotor 5i. If an Activity is launched as a "Payment method" from the Evotor "Sale" app, then `UposClientAidlInterface` does not react to `doSomething()` in that Activity:
https://github.com/SlavaGrishanin/evotor-upos-external-pinpad-issue/blob/master/app/src/main/java/ru/mars_groupe/sber_upos_example/MainActivity.kt

Video demonstration of the problem:
https://youtu.be/Z2_GnAwJlD8

Observations:

- Everything works correctly if the same Activity is launched from the launcher instead of the Evotor "Sale" menu: video 1:38-2:19
- The problem does not occur with the built-in PIN pad `ru.sberbank.uposnative`: video 2:25-3:08
- The problem does not occur if `UposVspClientAidlInterface` is used instead of `UposClientAidlInterface`: video 3:08-4:01
- However, with `UposVspClientAidlInterface` the built-in PIN pad Activity is not hidden: video 4:01-5:01

Open question: why does the external PIN pad not work with `UposClientAidlInterface` when it is used through the Evotor "Sale" menu?
