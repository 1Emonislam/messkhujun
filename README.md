# messkhujun

## otp send api: https://messkhujun.herokuapp.com/auth/otpSender

```
fetch('https://messkhujun.herokuapp.com/auth/otpSender',{
    method: 'POST',
    headers: {
    'Content-Type': 'application/json',
    }
    body:JSON.stringify({
    name,
    email,
    phone,
    gender,
    password,
    bio,
    pic
  }),
 })
```

## otp verify api: https://messkhujun.herokuapp.com/auth/otpVerify/:token //required paramas token

```
fetch('https://messkhujun.herokuapp.com/auth/otpVerify/:token',{
    method: 'POST',
    headers: {
    'Content-Type': 'application/json',
    },
    body:JSON.stringify({
    "otp":"23424"
})
    })
```

## phone password login api: https://messkhujun.herokuapp.com/auth/signIn

```
fetch('https://messkhujun.herokuapp.com/auth/signIn',{
    method: 'POST',
    headers: {
    'Content-Type': 'application/json',
    },
    body:JSON.stringify({
    "phone":"01943177541",
    "password":"123"
})
    })
```

## phone password reset api: https://messkhujun.herokuapp.com/auth/passwordResetSender

```
fetch('https://messkhujun.herokuapp.com/auth/passwordResetSender',{
    method: 'POST',
    headers: {
    'Content-Type': 'application/json',
    },
    body:JSON.stringify({
    "phone":"01943177541"
})
    })
```

## phone password reset code verify api: https://messkhujun.herokuapp.com/auth/passwordResetOtpVerify/:token

```
fetch('https://messkhujun.herokuapp.com/auth/passwordResetOtpVerify/:token',{
    method: 'POST',
    headers: {
    'Content-Type': 'application/json',
    },
    })
```

## get profile api: https://messkhujun.herokuapp.com/users/profile

```
fetch('https://messkhujun.herokuapp.com/users/profile',{
    method: 'GET',
    headers: {
    'Content-Type': 'application/json',
    'authorization': `Bearer ${token}` //required
    },

    })
```

## update profile api: https://messkhujun.herokuapp.com/users/profile

```
fetch('https://messkhujun.herokuapp.com/users/profile',{
    method: 'PUT',
    headers: {
    'Content-Type': 'application/json',
    'authorization': `Bearer ${token}` //required
    },
     body:JSON.stringify(bodyData)
    })
```

## get all users api: https://messkhujun.herokuapp.com/users/allUsers

```
fetch('https://messkhujun.herokuapp.com/users/allUsers',{
    method: 'GET',
    headers: {
    'Content-Type': 'application/json',
    },
```

## get all admins api: https://messkhujun.herokuapp.com/users/allAdmins

```
fetch('https://messkhujun.herokuapp.com/users/allAdmins',{
    method: 'GET',
    headers: {
    'Content-Type': 'application/json',
    'authorization': `Bearer ${token}` //required
    },
     body:JSON.stringify({
         "email": "abc@example.com"
     })
    })
```

## make admin api: https://messkhujun.herokuapp.com/users/makeAdmin

```
fetch('https://messkhujun.herokuapp.com/users/makeAdmin',{
    method: 'PUT',
    headers: {
    'Content-Type': 'application/json',
    'authorization': `Bearer ${token}` //required
    },
     body:JSON.stringify({
         "email":"abc@example.com"
     })
    })
```

## remove admin api: https://messkhujun.herokuapp.com/users/removeAdmin

```
fetch('https://messkhujun.herokuapp.com/users/removeAdmin',{
    method: 'PUT',
    headers: {
    'Content-Type': 'application/json',
    'authorization': `Bearer ${token}` //required
    },
     body:JSON.stringify({
         "email":"abc@example.com"
     })
    })
```

## create Mess Service api: https://messkhujun.herokuapp.com/mess/createMess

```
fetch('https://messkhujun.herokuapp.com/mess/createMess',{
    method: 'POST',
    headers: {
    'Content-Type': 'application/json',
    'authorization': `Bearer ${token}` //required
    },
    body:JSON.stringify({{
  "mess_root_Info":{
    "mess_owner_name":"Emon",
      "mess_owner_number":"01927837697",
        "mess_manger_name":"Emon",
          "mess_manger_string":"Islam"

  },
    "mess_information":{

      "messCreatedBy":"creater name",
        "mess_name":"abc mess",
          "location":"abc hotel 3230",
            "gio_location":"gio ip id",
              "area":"area cover ip address",
                "seat_available":"3"
    },
      "additional_information":{
        "dining_charge":"32",
          "wifi":"42",
          "total_seat":"3"

      },
        "rent_information":{
          "single_seat":"1",
            "double_seat":"2",
              "triple_seat":"3"
        },
          "meal_information":{
            "meal_rate":"34",
              "khala_bill":"32"
          },
            "other_Information":{
              "last_time":"Wed Jan 19 2022",
                "guest_allowed":"3",
                  "floor":"4",
                    "upload_image":"url link",
                    "upload_image_gallery":["url1","url2","url3"]
            },
              "reviews":[]

}
)
    })
```

## Update Mess Service api: https://messkhujun.herokuapp.com/mess/updateMess/_id

```
fetch('https://messkhujun.herokuapp.com/mess/updateMess/_id',{
    method: 'PUT',
    headers: {
    'Content-Type': 'application/json',
    'authorization': `Bearer ${token}` //required
    },
    body:JSON.stringify({{
  "mess_root_Info":{
    "mess_owner_name":"Emon",
      "mess_owner_number":"01927837697",
        "mess_manger_name":"Emon",
          "mess_manger_string":"Islam"

  },
    "mess_information":{

      "messCreatedBy":"creater name",
        "mess_name":"abc mess",
          "location":"abc hotel 3230",
            "gio_location":"gio ip id",
              "area":"area cover ip address",
                "seat_available":"3"
    },
      "additional_information":{
        "dining_charge":"32",
          "wifi":"42",
          "total_seat":"3"

      },
        "rent_information":{
          "single_seat":"1",
            "double_seat":"2",
              "triple_seat":"3"
        },
          "meal_information":{
            "meal_rate":"34",
              "khala_bill":"32"
          },
            "other_Information":{
              "last_time":"Wed Jan 19 2022",
                "guest_allowed":"3",
                  "floor":"4",
                    "upload_image":"url link",
                    "upload_image_gallery":["url1","url2","url3"]
            },
              "reviews":[]

}
)
    })
```

## get single mess api: https://messkhujun.herokuapp.com/mess/:id

```
fetch('https://messkhujun.herokuapp.com/mess/:id',{
    method: 'GET',
    headers: {
    'Content-Type': 'application/json',
    'authorization': `Bearer ${token}` //required
    },
    })
```

## Delete mess api: https://messkhujun.herokuapp.com/mess/:_id

```
fetch('https://messkhujun.herokuapp.com/mess/:_id',{
    method: 'DELETE',
    headers: {
    'Content-Type': 'application/json',
    'authorization': `Bearer ${token}` //required
    },
    })
```

## Get all mess api: https://messkhujun.herokuapp.com/mess

```
fetch('https://messkhujun.herokuapp.com/mess',{
    method: 'GET',
    headers: {
    'Content-Type': 'application/json',
    'authorization': `Bearer ${token}` //required
    },
    })
```

## review specification user mess api: https://messkhujun.herokuapp.com/mess/reviewsAdd/_id

```
fetch('https://messkhujun.herokuapp.com/mess/reviewsAdd/_id',{
    method: 'PUT',
    headers: {
    'Content-Type': 'application/json',
    'authorization': `Bearer ${token}` //required
    },
    body:JSON.stringify({
    "rating":"4",
    "comment":"good service"

})
    })
```

## get my reviews api: https://messkhujun.herokuapp.com/users/myReviews

```
fetch('https://messkhujun.herokuapp.com/users/myReviews',{
    method: 'GET',
    headers: {
    'Content-Type': 'application/json',
    'authorization': `Bearer ${token}` //required
    },
    })
```

## update my reviews api: https://messkhujun.herokuapp.com/users/myReviewsUpdate/:messId

```
fetch('https://messkhujun.herokuapp.com/users/myReviewsUpdate/:messId',{
    method: 'PUT',
    headers: {
    'Content-Type': 'application/json',
    'authorization': `Bearer ${token}` //required
    },
     body:JSON.stringify({
    "rating":"4",
    "comment":"good service"
})
    })
```

## add my favorite list api: https://messkhujun.herokuapp.com/users/favouriteListAdd/:_id

```
fetch('https://messkhujun.herokuapp.com/users/favouriteListAdd/:_id',{
    method: 'PUT',
    headers: {
    'Content-Type': 'application/json',
    'authorization': `Bearer ${token}` //required
    },
    })
```

## get my favorite list api: https://messkhujun.herokuapp.com/users/myfavouriteListGet

```
fetch('https://messkhujun.herokuapp.com/users/myfavouriteListGet',{
    method: 'GET',
    headers: {
    'Content-Type': 'application/json',
    'authorization': `Bearer ${token}` //required
    },
    })
```

## delete my favorite list api: https://messkhujun.herokuapp.com/users/favouriteListRemove/:_id

```
fetch('https://messkhujun.herokuapp.com/users/favouriteListRemove/:_id',{
    method: 'DELETE',
    headers: {
    'Content-Type': 'application/json',
    'authorization': `Bearer ${token}` //required
    },
    })
```
