---
title: "Contact"
layout: contact
hidemeta: true
description: "Any questions?  Please don't hesitate to send me an email through the following form!"
weight:
slug: ""
draft: false # 是否为草稿
comments: true
reward: false
showToc: false # 显示目录
TocOpen: false # 自动展开目录
disableShare: true # 底部不显示分享栏
showbreadcrumbs: false
cover:
    image: ""
    caption: ""
    alt: ""
    relative: false
---

<form method="post" action="https://formspree.io/f/myyazrqw">
  <div class="form-group row">
    <label for="name" class="col-4 col-form-label">Name</label>
    <div class="col-8">
      <div class="input-group">
        <div class="input-group-addon">
          <i class="fa fa-user"></i>
        </div>
        <input id="name" name="name" placeholder="Please enter your name" type="text" required="required" class="form-control", color=#FFFFFF>
      </div>
    </div>
  </div>
  <div class="form-group row">
    <label for="email" class="col-4 col-form-label">E-mail address</label>
    <div class="col-8">
      <div class="input-group">
        <div class="input-group-addon">
          <i class="fa fa-envelope"></i>
        </div>
        <input id="email" name="email" placeholder="Your e-mail address" type="text" required="required" class="form-control">
      </div>
    </div>
  </div>
  <div class="form-group row">
    <label for="message" class="col-4 col-form-label">Message</label>
    <p style="border-width:2px; border-style:solid; border-color:#FFFFFF; padding: 1em;">
      <textarea id="message" name="message" cols="61" rows="6" required="required" class="form-control"></textarea>
    </p>
  </div>
  <div class="form-group row">
    <div class="offset-4 col-8">
      <button name="submit" type="submit" class="btn btn-primary">Send</button>
    </div>
  </div>
</form>