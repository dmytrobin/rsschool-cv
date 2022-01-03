# Dmytro Binyk

---

![Avatar](/assets/img/avatar1.jpg)

---

### Position

**Junior Frontend Developer**

---

_Date of birth:_ 03.08.1981

_Place of birth:_ Ukraine, Lviv

_Current location:_ Ukraine, Kyiv

---

### Contacts

_Phone:_ +380504465331

_email:_ dmytro.binyk@gmail.com

_Telegram:_ @DimaBin

_LinkedIn:_ [Dmytro Binyk](https://www.linkedin.com/in/dmytro-binyk-74415732/)

---

### About me

I used to work for couple IT companies as a telecommunication engineer, network engineer, helpdesk support L1 engineer and IT manager. In addition, I created an e-commerce site using Codeigniter framework. After this, I owned furniture workshop for several years that I decided to close. Now, I am looking for opportunities to return to IT.

---

### Skills

- PHP
- HTML
- MySQL
- JavaScript
- CSS
- jQuery
- XML
- MongoDB
- Network equipment and protocols
- REXX
- Google script
- VBA
- Websites scrapping using Zennoposter and C#

---

### Code example

_JS function for fast checkout_

```js
$(document).ready(function () {
  var phone_last_enter = 10;
  var phone_last_enter = $("input[name=fast_order_contact]").val();
  if (phone_last_enter.length == 10) {
    $(".send").removeAttr("disabled");
    $(".send").css("opacity", "1");
  } else {
    $(".send").css("opacity", "0.5");
    $(".send").attr("disabled", "disabled");
  }
  $(".modal").colorbox({ inline: true, width: "30%" });
  $("#click").click(function () {
    var name = $("input[name=yourname]").val();
    var contact = $("input[name=contact]").val();
    var contact_len = contact.length;
    if (contact_len == 10) {
      $("input[name=contact]").css("background", "white");
      $("input[name=contact]").css("color", "#5F0054");
      $.ajax({
        type: "POST",
        url: baseurl + "email/fastcall",
        data: { name: name, contact: contact },
        success: function (data) {
          $("div #onee").html(data);
        },
      });
    } else {
      $("input[name=contact]").css("background", "#F59DB2");
      $("input[name=contact]").css("color", "white");
    }
  });

  $(".modal_fast_order").colorbox({ inline: true, width: "30%" });

  var phone = $("input[name=fast_order_contact]").keyup(function () {
    var phoneone = $("input[name=fast_order_contact]").val();
    var len = phoneone.length;
    if (len == 10) {
      $(".hide_notification").css("display", "none");
      $("input[name=fast_order_contact]").css("background", "white");
      $(".send").css("opacity", "1");
      $("input[name=fast_order_contact]").css("color", "#5F0054");
      $(".send").removeAttr("disabled");
    } else {
      $(".hide_notification").css("display", "inline");
      $("input[name=fast_order_contact]").css("background", "#F59DB2");
      $(".send").css("opacity", "0.5");
      $("input[name=fast_order_contact]").css("color", "white");
      $(".send").attr("disabled", "disabled");
    }
  });
  $("#send_p").on("click", ".send", function () {
    var product_id = $("input[name=product_id]").val();
    var phone = $("input[name=fast_order_contact]").val();

    $.ajax({
      type: "POST",
      url: baseurl + "fast_order/fastcall",
      data: { product_id: product_id, phone: phone },

      success: function (data) {
        $("div #fastcall").html(data);
      },
    });
  });
});
```

---

### Education

Computer Networking, Lviv Polytechnic National University, 1998-2003

---

### Courses

- devclub.com.ua [PHP]
- pozitiw.kiev.ua [PHP]

---

### Language Skills

IELTS Overall band 6.5

---
