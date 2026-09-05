# Day1 (25/8/2026)

I first started with planning how exactly I am going to make my keyboard,
I decided I was going to have a 60% keyboard with 61 keys
for This keyboard I am using the 'RaspberryPi_Pico' and I am planning on using matrix for my keyboard.
Today I created my full schematic
<img width="601" height="513" alt="Screenshot 2026-08-25 164051" src="https://github.com/user-attachments/assets/54f83247-54a5-45f7-8e01-2c73d5530eba" />
<img width="1374" height="681" alt="Screenshot 2026-08-25 164124" src="https://github.com/user-attachments/assets/3e4a91b2-561a-4200-badb-dd13da6e496e" />
<img width="1141" height="792" alt="image" src="https://github.com/user-attachments/assets/65b84c54-b87e-4e18-9f20-3ec5d29ad432" />

Hours spent today: 2 hours 15 minutes

___

# Day2 (26/8/2026)
I started my pcb layout as what I had planned earlier before. When I finished my layout I asked a friend I met on hack club for feedback, He told me that the switches weren't evenly spaced and told me that I had to replace all of the keys and that i had used a few extra stabalizers.
<img width="1385" height="621" alt="Screenshot 2026-08-26 124632" src="https://github.com/user-attachments/assets/b108c57b-9d35-41c4-a0e1-ed26439fa688" />
(this is how it looked like, it took me so long to manually place each of the keys)

Then I was told to use a plugin which could help me layout my keys, it was quite difficult navigating in the PCB since this was my first time using it, anyways once i used the plugin it made it much easier for me, the keys all positioned.
<img width="1354" height="471" alt="Screenshot 2026-08-26 155323" src="https://github.com/user-attachments/assets/7f8518e8-13cd-4914-96ad-3e100b78e210" />
Then I asked him for feedback and improvement he said to rotate the diode 90 degrees and repositioned it, i kept repositioning it until I got what I was looking for
<img width="862" height="601" alt="Screenshot 2026-08-26 161609" src="https://github.com/user-attachments/assets/7cf73ef1-d1ca-44be-9bb1-e2b7c1690f19" />

(this is what i got after mutiple tries of repositioning)
<img width="1446" height="560" alt="Screenshot 2026-08-26 183753" src="https://github.com/user-attachments/assets/0464b2aa-5148-471b-a145-b20cc108b17e" />

Then once again feedback, he told me to change the side of the diode(put it on the right of the switch since it would be much easier to route them.
<img width="1392" height="807" alt="Screenshot 2026-08-26 211512" src="https://github.com/user-attachments/assets/2c4bc0c8-151f-4676-a391-4cd3c54a9d1d" />
today I finished the layout, diode and switch placement throught today I learnt lots of new tools.

Hours spent today: 4 Hours 30 minutes 

___

# day 3 (27/8/2026)

Today I had started with the matrix and the routings
Fist I had learnt how to use the route single track feature then started with the columns then i connected the row
<img width="957" height="309" alt="image" src="https://github.com/user-attachments/assets/2e8fa437-8072-4364-b410-5e01cb408abb" />
It looked good, But once I connected the first wire to the raspberryPi_pico, I readlized that my rows weren't apperaing and there were lots of col 0 instead in many pins 
<img width="829" height="615" alt="Screenshot 2026-08-27 155812" src="https://github.com/user-attachments/assets/e8ff4449-ef4d-43cf-9278-6cc0c293da49" />
So I tried trouble shooting it and finding a solution, I first went back to my schematic to save it and update it in pcb, but that didn't work, then i realized that pins which weren't being used was marked x in the guide so I implemented that.

this is the picture in the guide <img width="625" height="744" alt="image" src="https://github.com/user-attachments/assets/1159da09-3b8c-4665-805f-ac97e6a9177c" />

However that still didnt work, but I asked my friend for help on it, he said that there was no ground pin and that might be the reason to it. once i replaced the x with the ground pin I thought it was all solved, but still didn't change the col0

<img width="334" height="430" alt="Screenshot 2026-08-27 162905" src="https://github.com/user-attachments/assets/4432d61e-19f5-44d4-accd-a75f9120e28f" />

I was looking at each switch in my schematic and noticed that I was actually short cicuiting it, I was adding the rows in the slot of the switches instead of the diode and was connecting each row to col0
<img width="1137" height="748" alt="Screenshot 2026-08-27 080918" src="https://github.com/user-attachments/assets/af47441c-b59c-4c28-97c6-ae3070dd4fe3" />

then i made the changes and it finally worked!!

<img width="1278" height="609" alt="Screenshot 2026-08-27 162152" src="https://github.com/user-attachments/assets/62f0a787-d819-468a-b240-db37252a2511" />
<img width="706" height="793" alt="Screenshot 2026-08-27 163529" src="https://github.com/user-attachments/assets/3ae659b3-5e7c-4b8f-b7e6-7d3815dafd39" />

then I connected/routed all of the wires to the RaspberryPi_pico,
Once i finished I checked design rule checker but got some errors (gnd pins weren't connected)
then I asked my friend for feedback again on the pcb, He told me to grnd both the copper plates
I went back to the guide and learnt how to do it, but still got errors, and I realized that while making the connections I had extended the cut and the pico's cable wouldn't fit, so I had moved it up and attached the routes to it, luckily the routes were just a few cm away.

<img width="1173" height="453" alt="Screenshot 2026-08-27 181951" src="https://github.com/user-attachments/assets/9beecb98-cf8d-43cc-b0cd-d486b4ca58b2" />

Once i finished I started planning my mounting holes and there was verry less space, 
<img width="1322" height="452" alt="Screenshot 2026-08-27 192502" src="https://github.com/user-attachments/assets/39b25a47-ed3f-4cf7-ae2a-b07d388b2d98" />

While adding it I learnt how use the move precisley feature (shift+m)
and used it to exactly position my mounting holes

<img width="879" height="298" alt="Screenshot 2026-08-27 194008" src="https://github.com/user-attachments/assets/f52e8452-c5ad-41db-9e9a-658b29e402a7" />

hours spent today in total: 6 hours

___

# Day 4 (4/9/2026)

I had took like a week brake since I had my exams

Today, I added footprints like the Cherry Mx switches and the keycaps and stabalizer to each slot
sadly I had to manually position each switch, key cap and stabilizer in each slot since I hadn't set footprints earlier so it took quite some time to place each one manually

Switches

<img width="505" height="398" alt="Screenshot 2026-08-28 100625" src="https://github.com/user-attachments/assets/032be3a9-47de-4f5c-a30d-e9c684784ed5" />
<img width="1102" height="611" alt="Screenshot 2026-08-28 121550" src="https://github.com/user-attachments/assets/4f47cac6-8fcc-404b-b048-74b4576f1bad" />
<img width="1219" height="392" alt="Screenshot 2026-08-28 160802" src="https://github.com/user-attachments/assets/2b14ef03-5ea6-40b4-8936-e1aa10708141" />

Keycaps and stabalizer

<img width="1161" height="422" alt="Screenshot 2026-08-29 085342" src="https://github.com/user-attachments/assets/eb9b26f4-a53e-4eb0-a5d6-d14835b88733" />

(while making the stabilizers first i had positioned them facing backwards(the wire) so then I had to rotate each, but luckly this time I only had to rotate 5)

<img width="1289" height="449" alt="Screenshot 2026-08-29 103915" src="https://github.com/user-attachments/assets/39f0384d-0f9a-4b75-ae45-2e9fefb37ec7" />

Then I learnt how to import to fusion, At first it wasn't working I tried different methords then I finally found why it wasn't uploading to fusion, I learnt that if it is in the KiCad file, it won't let you upload, so I draged my step file to dowanloads then it worked

Hours spent today: 2 Hours 30 minutes

___

# Day 5 (5/9/2026)

Today I started with the 3d model

First I started by making the case border, while making it I added some extra space in the bottom for the hot swaps to go there and fit, then I made the plate, While making it I added a .1mm kerf for the slots because I am going to be 3d printing it and since filament like PLA can expand a little and because 3d printing isn't perfect, I used section analysis a lot and it helped me so much it also made stuff easier anyways, I expanded the plate so that its the same size as the case and would work for my sandwich mount  
