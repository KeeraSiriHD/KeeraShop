local GUI = loadstring(game:HttpGet("https://raw.githubusercontent.com/Patskorn/GUI/main/Daino.lua"))()
local idk = GUI:new()
local win = idk:Tap("Keera HUB")


win:Button("Webhook my Discord test",function()
    setclipboard("https://discord.com/api/webhooks/967142850158542901/mBycpiIYrU0bBjmRnpbX36SxCDw3R-kRA5kKHRw0We5RmiIBC7CvHoYMigsfToJfWW_o")
end)



local win = idk:Tap("Misc")
win:Label("Misc can use all map")




win:Button("RTX MODE(on)",function()
   	local a = game.Lighting
	a.Ambient = Color3.fromRGB(33, 33, 33)
	a.Brightness = 6.67
	a.ColorShift_Bottom = Color3.fromRGB(0, 0, 0)
	a.ColorShift_Top = Color3.fromRGB(255, 247, 237)
	a.EnvironmentDiffuseScale = 0.105
	a.EnvironmentSpecularScale = 0.522
	a.GlobalShadows = true
	a.OutdoorAmbient = Color3.fromRGB(51, 54, 67)
	a.ShadowSoftness = 0.04
	a.GeographicLatitude = -15.525
	a.ExposureCompensation = 0.75
	local b = Instance.new("BloomEffect", a)
	b.Enabled = true
	b.Intensity = 0.04
	b.Size = 1900
	b.Threshold = 0.915
	local c = Instance.new("ColorCorrectionEffect", a)
	c.Brightness = 0.176
	c.Contrast = 0.39
	c.Enabled = true
	c.Saturation = 0.2
	c.TintColor = Color3.fromRGB(217, 145, 57)
	if getgenv().mode == "Summer" then
		c.TintColor = Color3.fromRGB(255, 220, 148)
	elseif getgenv().mode == "Autumn" then
		c.TintColor = Color3.fromRGB(217, 145, 57)
	else
		warn("No mode selected!")
		print("Please select a mode")
		b:Destroy()
		c:Destroy()
	end
	local d = Instance.new("DepthOfFieldEffect", a)
	d.Enabled = true
	d.FarIntensity = 0.077
	d.FocusDistance = 21.54
	d.InFocusRadius = 20.77
	d.NearIntensity = 0.277
	local e = Instance.new("ColorCorrectionEffect", a)
	e.Brightness = 0
	e.Contrast = -0.07
	e.Saturation = 0
	e.Enabled = true
	e.TintColor = Color3.fromRGB(255, 247, 239)
	local e2 = Instance.new("ColorCorrectionEffect", a)
	e2.Brightness = 0.2
	e2.Contrast = 0.45
	e2.Saturation = -0.1
	e2.Enabled = true
	e2.TintColor = Color3.fromRGB(255, 255, 255)
	local s = Instance.new("SunRaysEffect", a)
	s.Enabled = true
	s.Intensity = 0.01
	s.Spread = 0.146
end)


win:Button("RTX MODE(off)",function()
   	local light = game.Lighting
	for i, v in pairs(light:GetChildren()) do
		v:Destroy()
	end

	local ter = workspace.Terrain
	local color = Instance.new("ColorCorrectionEffect")
	local bloom = Instance.new("BloomEffect")
	local sun = Instance.new("SunRaysEffect")
	local blur = Instance.new("BlurEffect")

	color.Parent = light
	bloom.Parent = light
	sun.Parent = light
	blur.Parent = light


	local config = {

		Terrain = true;
		ColorCorrection = true;
		Sun = true;
		Lighting = true;
		BloomEffect = true;

	}


	color.Enabled = false
	color.Contrast = 0.15
	color.Brightness = 0.1
	color.Saturation = 0.25
	color.TintColor = Color3.fromRGB(255, 222, 211)

	bloom.Enabled = false
	bloom.Intensity = 0.1

	sun.Enabled = false
	sun.Intensity = 0.2
	sun.Spread = 1

	bloom.Enabled = false
	bloom.Intensity = 0.05
	bloom.Size = 32
	bloom.Threshold = 1

	blur.Enabled = false
	blur.Size = 6



	if config.ColorCorrection then
		color.Enabled = true
	end


	if config.Sun then
		sun.Enabled = true
	end


	if config.Terrain then
		ter.WaterColor = Color3.fromRGB(10, 10, 24)
		ter.WaterWaveSize = 0.1
		ter.WaterWaveSpeed = 22
		ter.WaterTransparency = 0.9
		ter.WaterReflectance = 0.05
	end


	if config.Lighting then
		light.Ambient = Color3.fromRGB(0, 0, 0)
		light.Brightness = 4
		light.ColorShift_Bottom = Color3.fromRGB(0, 0, 0)
		light.ColorShift_Top = Color3.fromRGB(0, 0, 0)
		light.ExposureCompensation = 0
		light.FogColor = Color3.fromRGB(132, 132, 132)
		light.GlobalShadows = true
		light.OutdoorAmbient = Color3.fromRGB(112, 117, 128)
		light.Outlines = false
		
	end

end)

win:Button("หมัดไฟFiveM",function()
    local Fire = Instance.new("Fire")
Fire.Parent = game.Players.LocalPlayer.Character.RightHand
Fire.Heat = 5
Fire.Size = 2
end)




win:Button("Tool TP(ใช้ได้ทุกmapแต่บางแมพต้องใช้bypass TP)",function()
    mouse = game.Players.LocalPlayer:GetMouse()
tool = Instance.new("Tool")
tool.RequiresHandle = false
tool.Name = "tool TP"
tool.Activated:connect(function()
local pos = mouse.Hit+Vector3.new(0,2.5,0)
pos = CFrame.new(pos.X,pos.Y,pos.Z)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = pos
end)
tool.Parent = game.Players.LocalPlayer.Backpack
end)
   
   
win:Button("Https Spy",function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/Patskorn/Teleport/main/https-spy.lua"))()
end)


local win = idk:Tap("script YBA")


win:Label("รวม script YBA ตุงๆ")

win:Button("Xenon",function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/KeeraSiriHD/XenonYBA/main/README.md"))()
end)

win:Button("YBA cuz yes",function()
    getgenv().Key = "HelloEpicGUI"
    loadstring(game:HttpGet("https://raw.githubusercontent.com/SupBabe/YBAHOPPER/main/YBAv2.lua"))()
end)


win:Label("Teleport(ใช้scriptก่อนใช้งาน)")
win:Button("TP(lvl 1+)",function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(83.4876709, 825.811218, -93.6656799, -7.57965335e-09, -0.17340225, 0.984851241, 1, -4.37113883e-08, 0, 4.30492157e-08, 0.984851241, 0.17340225)
end)


win:Button("TP(lvl 1+)",function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(691.426758, 803.46051, -219.359894, -4.22221262e-08, -0.965929627, 0.258804798, 1, -4.37113883e-08, 0, 1.1312717e-08, 0.258804798, 0.965929627)
end)


win:Button("TP(lvl 10+)",function()
     game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(153.279404, 825.810974, 213.341202, -2.62150834e-08, -0.599731207, 0.800201535, 1, -4.37113883e-08, 0, 3.49779192e-08, 0.800201535, 0.599731207)
end)


win:Button("TP(lvl 15+)",function()
     game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-225.805298, 825.811279, 153.951874, 1.50030761e-08, 0.343230367, 0.939251244, 1, -4.37113883e-08, 0, 4.10559764e-08, 0.939251244, -0.343230367)
end)



win:Button("TP(lvl 20+)",function()
     game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(84.7772522, 734.801331, 35.4892883, -2.50937084e-08, -0.574077129, 0.818801284, 1, -4.37113883e-08, 0, 3.579094e-08, 0.818801284, 0.574077129)
end)


win:Button("TP(lvl 30+)",function()
     game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(501.724487, 928.811279, -58.7153168, 8.59453576e-05, -0.984570861, -0.174986392, 1, 8.59446809e-05, 7.58189117e-06, 7.57424232e-06, -0.174986392, 0.984570861)
end)


win:Button("TP(lvl 35+)",function()
     game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(824.500549, 803.401855, -80.0057907, -0.000424200174, 0.087131381, -0.996196747, 0.999999881, -4.23924175e-05, -0.000429527427, -7.96564927e-05, -0.996196866, -0.0871312618)
end)


win:Button("TP(lvl 40+)",function()
     game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(61.7582703, 821.461243, 877.547852, -4.37113883e-08, -1, 0, 1, -4.37113883e-08, 0, 0, 0, 1)
end)





local win = idk:Tap("Star Tower Defense")

win:Button("riverhub",function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/Arshishi/korn/main/K1",true))();
end)

win:Button("Copy riverhub(เอสไปใส่Autoexec)",function()
    setclipboard("https://pastebin.com/raw/WdgrSyQ5")
end)


local win = idk:Tap("Stand Upright: Rebooted")


win:Button("Lazy Hub(OP)",function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/LioK251/Scripts/main/"..game.PlaceId..".lua"))()
end)


win:Button("Noob Upright",function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/Kaiden00/Scripts/main/thingy"))()
end)
 
 
win:Button("IDK",function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/LioK251/Scripts/main/"..game.PlaceId..".lua"))()
end)




local win = idk:Tap("blox fruit")


win:Label("script blox fruit")

win:Button("MUKURO",function()
    loadstring(game:HttpGet"https://raw.githubusercontent.com/xDepressionx/Free-Script/main/AllScript.lua")()
end)
 
win:Button("MARKXHub",function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/ArceusXHub/AV2022/main/README.md", true))()
end)


win:Button("PowerxCANDYYY",function()
    _G.Color = Color3.fromRGB(255,255,255)
    loadstring(game:HttpGet("https://raw.githubusercontent.com/PowerxCANDYYY/NaMo/main/BFPOWERXHUBv2.lua"))()
end)

local win = idk:Tap("Vehicle Legends(coming soon)")
local win = idk:Tap("The Mimic(coming soon)")
local win = idk:Tap("Pet Simulator X! 🐾(coming soon)")
local win = idk:Tap("🔥 Zombie Uprising🔥(coming soon)")
local win = idk:Tap("Da Hood(coming soon)")
local win = idk:Tap("Anime Fighters Simulator(coming soon)")
local win = idk:Tap("(coming soon)")
local win = idk:Tap("(coming soon)")

