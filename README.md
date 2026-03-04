# hydroqc

This repository contains my Home Assistant optimisations in order to minimise energy consumption and maximise winter credits offered by Hydro Quebec to customers that join the Rate D - Winter Credit plan, also known as CPC option. You can learn more about how the Winter Credit Option works [here](https://github.com/illigtr/hydroqc/wiki/Understanding-How-Hydro-Quebec's-Winter-Credit-Option-Works)

Historically, I started optimising energy well before HQ introduced the WCO program and even before I had Home Assistant. My goal was to optimise a 35 year old Lennox heat pump that had an energy inefficient timer-based defrost board. Since each forced defrost cycle after 30 minutes of heat pump run time, wastes significant energy (basically heating the outdoors and cooling the indoors -- in winter), I built a new defrost board based on ESP32. This board only defrosted the outdoor coils when necessary and I was able to save about $300 of electrical energy annually.

Since this project forced me to monitor energy consumption on the heat pump, the electric furnace and other room heating, I extended the project to modify heating patterns when the Winter Credit Option was first introduced as a pilot project. I finally migrated all my custom ESP32 based heating controls over to ESPHome and Home Assistant.

Since 2020, every year, the optimisations have improved, energy consumption has decreased and WCO credit $ have increased. I am sharing these optimisations to anyone having Home Assistant with sensors and controls for energy consumption and home heating.

This year, an addtional tool was built: The [WCO simulator and validator spreadsheet](https://github.com/illigtr/hydroqc/blob/main/WCO%20Validation%20Simulator%20Tool%20-%20v5.2.xlsm). Click on the link, then use the download button in Github to download the spreadsheet to your computer. This tool can fetch a user's winter credit details and full hourly consumption history to validate that your credits are calcuated propertly by Hydro Quebec. Furthermore, the tool allows a user to run "what-if" scenarios in order to determine the best parameters for energy savings all the while maximising credit $ available from Hydro Quebec under the program.

>
> If you are only interested in using the Simulator/Validator tool, you'll find instructions for the Simulator [here](https://github.com/illigtr/hydroqc/wiki/The-Simulator-Tool), and for the Validator [here](https://github.com/illigtr/hydroqc/wiki/Using-the-Validator-Tool). I appreciate any feedback and if issues are found, please open on issue in Github.
>


Please see the [Wiki](https://github.com/illigtr/hydroqc/wiki) for detailed instruction and explanations of the HA optimisations and WCO simulator and validator spreadsheet

## A word from the author.
> The author does not work, directly or indirectly with Hydro Quebec. The tools here in are in no way associated with Hydro Quebec.
>
> ***Under no circumstances does the author condone or encourage the abuse of the Hydro Quebec Winter Credit Option by wasteful energy usage for the sole purpose of deriving credit dollars.***

### License

> This code is released into the public domain for non-commercial use.
> 
> Permission is granted to copy, modify, and redistribute this code, provided
> that proper credit is given to the original author in any derivative works
> or redistributed versions.
> This code is provided "as is" without warranty of any kind, express or
> implied. The author shall not be held liable for any damages, losses, or
> other issues arising from the use, misuse, or inability to use this code.
>
> Commercial use requires prior written permission from the author.

