DayZ Namalsk PC "RedFalcon Watercraft" Mod by RedFalcon PC Install Instructions & Terms Of Use

Many thanks to RedFalcon for creating this amazing mod. Please visit his Discord, https://discord.io/redfalconmodz
and sub to his YouTube: https://www.youtube.com/channel/UCznA3EuyfHuISNjqtNOs0jg

Many Thanks to Adam Francu for his amazing Namalsk Mod. https://www.twitch.tv/namalsksurvivor

THIS IS AN EARLY SET OF FILES SO SERVER OWNERS CAN EASILY SPAWN IN FULLY WORKING BOATS WITHOUT USING ADMIN TOOLS OR TRADER.
THESE FILES WILL PROBABLY BE SUPERCEDED AS RED FALCON CREATES HIS OWN XMLS.

Spawns four types of fully working (you just need to add fuel and oil, which is included in cargo) boats at various points on the coast of Namalsk. (See photos in Github)

AT TIME OF RELEASE THESE BOATS ONLY WORK ON THE OCEAN AND NOT RIVERS OR LAKES, SO THEY WILL NOT WORK ON LIVONIA.

THIS IS NOT RedFalcon's OFFICIAL INSTALL INSTRUCTIONS AND IS NOT AFFILIATED WITH RED FALCON.

Limited Testing on PC Namalsk Local Server & Nitrado Community PC Server DAYZ Version 1.19 Dec 2022.

XML snippets Created by @scalespeeder. Please report bugs & errors to scalespeeder@gmail.com with screenshots.

TERMS OF USE
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

PLEASE SEE THE README INSIDE THE RedFalcon Watercraft MOD FOR RedFalcon's TERMS OF USE.

Using these modded xml / json files and instructions could break the functioning of your DAYZ server, requiring a reinstall that would wipe
all player progress.

Using these modded files neccessitates increased regular restarts to prevent server crashing.

It is suggested you thoroughly test your server after applying these files to ensure proper
functioning of your server.

I always recomend you validate your files at: https://www.xmlvalidation.com/ and https://jsonformatter.curiousconcept.com/

Instructions:

Subscribe to & install Namalsk Survival & Namalsk Island on Steam: (See Steam for intsall instructions)

https://steamcommunity.com/workshop/filedetails/?id=2289456201

https://steamcommunity.com/sharedfiles/filedetails/?id=2289461232

Subscribe to RedFalcon Watercraft on Steam:

https://steamcommunity.com/sharedfiles/filedetails/?id=2906371600

Start your DayZ Launcher to download the mod files. Using your FTP programme, copy the @RedFalcon Watercraft folder from your DayZ !workshop folder
to the root directory of your server. Copy the key from the mods key folder to your servers key folder. Edit your start batch file,
so that your server will load @RedFalcon Watercraft mod on startup. (On Nitrado and some other DayZ Server Providers you don't have access to the batch file,
instead you will find an "Additional mods" setting in the settings section of your servers web interface, add @RedFalcon Watercraft there.)

Click the "Code" button and "Download Zip" on the Github Repository and extract the files on your local PC for access. All the xml snippets you need are within this readme.

Stop your server using it's web control panel.

Using FTP or your Servers file browser, make the following additions to your XMLS:

Open your events.xml file (its in the db folder on your server) and add the following XML snippet at the top, below the <events> tag:

<!-- RedFalcon Watercraft events additions-->

 <event name="VehicleRFWC_Watercraft">
        <nominal>8</nominal>
        <min>8</min>
        <max>8</max>
        <lifetime>300</lifetime>
        <restock>0</restock>
        <saferadius>500</saferadius>
        <distanceradius>500</distanceradius>
        <cleanupradius>200</cleanupradius>
        <flags deletable="0" init_random="0" remove_damaged="1"/>
        <position>fixed</position>
        <limit>mixed</limit>
        <active>1</active>
        <children>
            <child lootmax="0" lootmin="0" max="2" min="2" type="RFWC_Whaler"/>
            <child lootmax="0" lootmin="0" max="2" min="2" type="RFWC_CarpBoat"/>
            <child lootmax="0" lootmin="0" max="2" min="2" type="RFWC_Zodiac_Black"/>
			<child lootmax="0" lootmin="0" max="2" min="2" type="RFWC_Zodiac_Orange"/>
        </children>
    </event>
	
<!-- end of RedFalcon Watercraft events additions -->


Open your types.xml file (its in the db folder on your server) and add the following XML snippet at the top, below the <types> tag:

<!-- RedFalcon Watercraft types additions-->
  <type name="RFWC_Whaler">
        <nominal>0</nominal>
        <lifetime>3888000</lifetime>
        <restock>0</restock>
        <min>0</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
    </type>
    <type name="RFWC_Whaler_Wreck">
        <nominal>0</nominal>
        <lifetime>3600</lifetime>
        <restock>0</restock>
        <min>0</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
    </type>
    <type name="RFWC_CarpBoat">
        <nominal>0</nominal>
        <lifetime>3888000</lifetime>
        <restock>0</restock>
        <min>0</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
    </type>
    <type name="RFWC_CarpBoat_Wreck">
        <nominal>0</nominal>
        <lifetime>3600</lifetime>
        <restock>0</restock>
        <min>0</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
    </type>
    <type name="RFWC_Zodiac_Black">
        <nominal>0</nominal>
        <lifetime>3888000</lifetime>
        <restock>0</restock>
        <min>0</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
    </type>
    <type name="RFWC_Zodiac_Black_Wreck">
        <nominal>0</nominal>
        <lifetime>3888000</lifetime>
        <restock>0</restock>
        <min>0</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
    </type>
    <type name="RFWC_Zodiac_Orange">
        <nominal>0</nominal>
        <lifetime>3888000</lifetime>
        <restock>0</restock>
        <min>0</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
    </type>
    <type name="RFWC_Zodiac_Orange_Wreck">
        <nominal>0</nominal>
        <lifetime>3600</lifetime>
        <restock>0</restock>
        <min>0</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
    </type>
    <type name="EngineOil">
        <nominal>40</nominal>
        <lifetime>28800</lifetime>
        <restock>0</restock>
        <min>30</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0" />
        <category name="tools" />
        <usage name="Industrial" />
        <tag name="floor" />
    </type>
	
	<!-- end of RedFalcon Watercraft types additions-->
	
Save the file and re-upload if necessary.

Open your cfgspawnabletypes.xml file (its in the root folder of the mission folder on your server) and add the following XML snippet,
just below <spawnabletypes> which is near the top of the file:

		<!-- start of RedFalcon Watercraft spawnabletypes -->
	
	<type name="RFWC_Whaler">
<attachments chance="1.00">
			<item name="RFWC_Anchor_Rope" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="SparkPlug" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="TruckBattery" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="CanisterGasoline" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="EngineOil" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="EngineOil" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="EngineOil" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="FishingRod" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Hook" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Hook" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="worm" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="worm" chance="1.00" />
		</attachments>
	</type>
	
	<type name="RFWC_CarpBoat">
	<attachments chance="1.00">
			<item name="RFWC_Anchor_Rope" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="SparkPlug" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="TruckBattery" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="CanisterGasoline" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="EngineOil" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="EngineOil" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="EngineOil" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="FishingRod" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Hook" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Hook" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="worm" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="worm" chance="1.00" />
		</attachments>
	</type>
	
	<type name="RFWC_Zodiac_Black">
	<attachments chance="1.00">
			<item name="RFWC_Anchor_Rope" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="SparkPlug" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="TruckBattery" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="CanisterGasoline" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="EngineOil" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="EngineOil" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="EngineOil" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="FishingRod" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Hook" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Hook" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="worm" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="worm" chance="1.00" />
		</attachments>
	</type>
	
	<type name="RFWC_Zodiac_Orange">
	<attachments chance="1.00">
			<item name="RFWC_Anchor_Rope" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="SparkPlug" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="TruckBattery" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="CanisterGasoline" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="EngineOil" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="EngineOil" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="EngineOil" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="FishingRod" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Hook" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Hook" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="worm" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="worm" chance="1.00" />
		</attachments>
	</type>
	
	
	<!--end of RedFalcon Watercraft spawnabletypes additions-->
	
	
	Open your cfgeventspawns.xml file (its in the root folder of the mission folder on your server) and add the following XML snippet,
just below <eventposdef> which is near the top of the file:
	
	<!-- RedFalcon Watercraft event spawns additions-->
	
<event name="VehicleRFWC_Watercraft">
		<pos x="5614.00" z="9916.42" a="1.736423" /> 
		<pos x="6258.87" z="9995.75" a="1.736423" />
		<pos x="6411.66" z="8497.33" a="32.092476" />
		<pos x="7935.46" z="7661.02" a="-36.527287" />
		<pos x="7780.02" z="5913.14" a="100.383453" />
		<pos x="5042.28" z="6057.22" a="0.000000" />
		<pos x="4332.77" z="4718.87" a="-13.206916" />
		<pos x="2139.01" z="6063.31" a="-142.020447" />
		</event>
	
<!-- end of RedFalcon Watercraft event spawns additions -->
	

Save your changes & upload if you need to.

Restart your server and the boats will be spawning in for the enjoyment of your players!!!!!

Thanks again to RED FALCON

Please join his Discord: https://discord.io/redfalconmodz
and sub to his YouTube: https://www.youtube.com/channel/UCznA3EuyfHuISNjqtNOs0jg 

Thanks, Rob.
