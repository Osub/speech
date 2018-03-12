## Introduction
    本项目是基于百度智能语音的SDK扩展封装为php的composer包

## Install
 `composer require machero/speech`

## Use
```php

    $speech = new AipSpeech(
        config('baidu-speech.app_id'),
        config('baidu-speech.app_key'),
        config('baidu-speech.app_secret')
    );
    $this->speech = $speech;
    /**
     * @apiparams $text 要合成的文本
     * @apiparams $spd  语音的速度
     *
     */
    $mp3 = $this->speech->synthesis($text, $lang='zh', $ctp=1, $options=array('spd'=>3));
    //具体请参考百度智能语音开发文档
```
