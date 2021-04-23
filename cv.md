# Omelchenko Aleksandr Vasilevich

**Android developer**
With the motto: "It's never too late to learn!"

### Contact Info

**E-mail:** omelchenkoaleks@gmail.com
**Telegram:** @omelchenkoaleks
**Phone:** +380630213634
**Skype:** om-koaleks

## Summary

Developing mobile apps opens up the opportunity for me to do something truly rewarding. It is very satisfying. It is very satisfying. I have a strong desire to make quality products that can be beneficial and make life easier. To do this, I set a goal for myself - to develop and learn to make everything more reliable and use the best technologies.

Shortly about myself. I have experience in self-study and skills to quickly search for information on the Internet. I try to get to the bottom of it in order to understand the subject, even if it takes longer than previously thought. For myself, I try to determine tasks according to the importance of their implementation and plan them.

## Skills

_programming languages:_ **Java** and **Kotlin**
_framework:_ **Android**
_patterns:_ **MVVM**, **MVP**, **MVC**
_version control:_ **GIT**
_tools:_ **Android Architecture Components**, **Android Jetpack**
_development environment_ **Android Studio**

## Code examples

    class AppVoiceRecorder {
    	private val mMediaRecorder = MediaRecorder()
    	private lateinit var mFile: File
    	private lateinit var mMessageKey: String

        fun startRecord(messageKey: String) {
            try {
                mMessageKey = messageKey
                createFileForRecord()
                prepareMediaRecorder()
                mMediaRecorder.start()
            } catch (e: Exception) {
                showToast(e.message.toString())
            }
        }

        private fun prepareMediaRecorder() {
            mMediaRecorder.apply {
              reset()
                setAudioSource(MediaRecorder.AudioSource.DEFAULT)
                setOutputFormat(MediaRecorder.OutputFormat.DEFAULT)
                setAudioEncoder(MediaRecorder.AudioEncoder.DEFAULT)
                setOutputFile(mFile.absolutePath)
                prepare()
            }
        }

        private fun createFileForRecord() {
            mFile = File(APP_ACTIVITY.filesDir, mMessageKey)
            mFile.createNewFile()
        }

        fun stopRecord(onSuccess: (file: File, messageKey: String) -> Unit) {
            try {
                mMediaRecorder.stop()
                onSuccess(mFile, mMessageKey)
            } catch (e: Exception) {
                showToast(e.message.toString())
                mFile.delete()
            }
        }

        fun releaseRecorder() {
            try {
                mMediaRecorder.release()
            } catch (e: Exception) {
                showToast(e.message.toString())
            }
        }
    }

## Experience

_git repositories:_ [omelchenkoaleks (github.com)](https://github.com/omelchenkoaleks)
_Google Play_ [Приложения в Google Play – Time Limit](https://play.google.com/store/apps/details?id=com.omelchenkoaleks.timerformeeting)
_Google Play_ [Приложения в Google Play – Android Architecture Components](https://play.google.com/store/apps/details?id=com.omelchenkoaleks.androidarchitecturecomponents)

## Education

_JetBrains Academy_ https://hyperskill.org/
_Udacity_ https://classroom.udacity.com/
_YouTube channels:_ **Android Broadcast**, **tutorialsEU**, **Rolling Scopes School :)**

## English

English beginner level
