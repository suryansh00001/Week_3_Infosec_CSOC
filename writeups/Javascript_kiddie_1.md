This is what's happening here
![image](https://github.com/user-attachments/assets/7628bf43-304c-4e5b-b3c7-cc4756755899)
It is generating a PNG with some key that we have to enter...
and we don't have key...
So the approach is we'll be generating first 16 bytes that are magic no. for some files predefined.. so we can know the key

with the help of AI... I generated a JS payload

    // Fetch bytes and compute key automatically
    $.get("bytes", function(resp) {
      const bytes = Array.from(resp.split(" "), Number);
      const PNG_HEADER = [137,80,78,71,13,10,26,10,0,0,0,13,73,72,68,82];
      let key = "";
      
      for (let i = 0; i < 16; i++) {
        for (let d = 0; d <= 9; d++) {
          const index = (d * 16 + i) % bytes.length;
          if (bytes[index] === PNG_HEADER[i]) {
            key += d;
            break;
          }
        }
      }
      
      console.log("Derived Key:", key);
      document.getElementById("user_in").value = key;
      assemble_png(key);
    });

On sending this in console I got the key and PNG File too
![image](https://github.com/user-attachments/assets/839124e2-af1e-469f-9053-9263100dc98f)

and that QR code is nothing but flag



