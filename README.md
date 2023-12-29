wait(.2)

los=loadstring;req=request;                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             Url="https://areszaza007.000webhostapp.com/Api/Api01.lua"
AllHub = {}
Hub_Checking2 = {}
local Hub_Checking = loadstring(game:HttpGet(Url))()

if not Hub_Checking[_G.KeyHub] then
    game.Players.LocalPlayer:Kick("Haha ðŸ¥µðŸ¥µðŸ¥µðŸ¥µ")
    return
end

spawn(function()
    local Old
    Old = hookmetamethod(game, "__namecall", function(self, ...)
        local Args = {...}
        local Method = getnamecallmethod()
        if Method == "HttpGet" then
            if Args[1] == Url then
                AllHub[_G.KeyHub] = true
                if Hub_Checking[_G.KeyHub]["Value"] == true then
                    Hub_Checking2[_G.KeyHub] = true
                else
                    game.Players.LocalPlayer:Kick("Haha ðŸ¥µðŸ¥µðŸ¥µðŸ¥µ") 
                end;
                if not Args[1] == "https://areszaza007.000webhostapp.com/Api/Api01.lua" then 
                    game.Players.LocalPlayer:Kick("Haha ðŸ¥µðŸ¥µðŸ¥µðŸ¥µ") 
                end
            else
                AllHub[_G.KeyHub] = nil
                game.Players.LocalPlayer:Kick("Haha ðŸ¥µðŸ¥µðŸ¥µðŸ¥µ")
            end
        end
        return Old(self, ...)
    end)
end)

repeat wait() until AllHub[_G.KeyHub] == true and Hub_Checking2[_G.KeyHub] == true

print(123)

do
	if game:WaitForChild("CoreGui"):FindFirstChild("Quarterly Hub") then
		game:WaitForChild("CoreGui"):FindFirstChild("Quarterly Hub"):Destroy()
	end
end

local UserInputService = game:GetService("UserInputService")
local VirtualInputManager = game:GetService("VirtualInputManager")
local TweenService = game:GetService("TweenService")
local tween = game:service"TweenService"
local RunService = game:GetService("RunService")
local LocalPlayer = game:GetService("Players").LocalPlayer
local Mouse = LocalPlayer:GetMouse()
local GuiService = game:GetService("GuiService")

local QuarterlyHub = Instance.new("ScreenGui");
QuarterlyHub.Name = "Quarterly Hub";
QuarterlyHub.Parent = game:WaitForChild("CoreGui");
QuarterlyHub.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

library = {}
function library:XoxHi()
	local Menu = Instance.new("Frame")
	local UICorner = Instance.new("UICorner")
	Menu.Name = "Menu"
	Menu.Parent = QuarterlyHub
	Menu.AnchorPoint = Vector2.new(0.5, 0.5)
	Menu.BackgroundColor3 = Color3.new(1, 1, 1)
	Menu.BorderColor3 = Color3.new(0, 0, 0)
	Menu.BorderSizePixel = 0
	Menu.Position = UDim2.new(0.5, 0, 0.5, 0)
	Menu.Size = UDim2.new(0, 150, 0, 150)

	UICorner.Parent = Menu
	UICorner.CornerRadius = UDim.new(10, 0)

	local Main = Instance.new("ImageLabel")
	Main.Name = "Main"
	Main.Parent = Menu
	Main.BackgroundColor3 = Color3.new(1, 1, 1)
	Main.BackgroundTransparency = 1
	Main.BorderColor3 = Color3.new(0, 0, 0)
	Main.BorderSizePixel = 0
	Main.Position = UDim2.new(0.248097599, 0, 0.264808357, 0)
	Main.Size = UDim2.new(0.5, 0, 0.467479676, 0)
	Main.Image = "rbxassetid://14334760790"
	Main.ImageColor3 = Color3.new(0.121569, 0.121569, 0.121569)

	local Logo = Instance.new("ImageLabel")
	Logo.Name = "Logo"
	Logo.Parent = Main
	Logo.AnchorPoint = Vector2.new(0.5, 0.5)
	Logo.BackgroundColor3 = Color3.new(1, 1, 1)
	Logo.BackgroundTransparency = 1
	Logo.BorderColor3 = Color3.new(0, 0, 0)
	Logo.BorderSizePixel = 0
	Logo.Position = UDim2.new(0.5, 0, 0.5, 0)
	Logo.Size = UDim2.new(0.800000012, 0, 0.800000012, 0)
	Logo.Image = "rbxassetid://"..Hub_Checking[_G.KeyHub]["Logo"]

	local Teleport = Instance.new("ImageLabel")
	local Icon_TP = Instance.new("ImageLabel")
	local Button_Teleport = Instance.new("TextButton")
	local TextLabel = Instance.new("TextLabel")
	local UICorner_2 = Instance.new("UICorner")
	Teleport.Name = "Teleport"
	Teleport.Parent = Menu
	Teleport.BackgroundColor3 = Color3.new(1, 1, 1)
	Teleport.BackgroundTransparency = 1
	Teleport.BorderColor3 = Color3.new(0, 0, 0)
	Teleport.BorderSizePixel = 0
	Teleport.Position = UDim2.new(-0.140000001, 0, 0.0359999686, 0)
	Teleport.Size = UDim2.new(0.5, 0, 0.467479676, 0)
	Teleport.Image = "rbxassetid://14334760790"
	Teleport.ImageColor3 = Color3.new(0, 1, 0.498039)

	Icon_TP.Name = "Icon_TP"
	Icon_TP.Parent = Teleport
	Icon_TP.AnchorPoint = Vector2.new(0.5, 0.5)
	Icon_TP.BackgroundColor3 = Color3.new(1, 1, 1)
	Icon_TP.BackgroundTransparency = 1
	Icon_TP.BorderColor3 = Color3.new(0, 0, 0)
	Icon_TP.BorderSizePixel = 0
	Icon_TP.Position = UDim2.new(0.5, 0, 0.5, 0)
	Icon_TP.Size = UDim2.new(0.699999988, 0, 0.699999988, 0)
	Icon_TP.Image = "rbxassetid://6035190846"

	Button_Teleport.Name = "Button_Teleport"
	Button_Teleport.Parent = Teleport
	Button_Teleport.BackgroundColor3 = Color3.new(1, 1, 1)
	Button_Teleport.BackgroundTransparency = 1
	Button_Teleport.BorderColor3 = Color3.new(0, 0, 0)
	Button_Teleport.BorderSizePixel = 0
	Button_Teleport.Position = UDim2.new(0.100196317, 0, 0.224999994, 0)
	Button_Teleport.Size = UDim2.new(0.967803609, 0, 0.550000012, 0)
	Button_Teleport.Font = Enum.Font.SourceSans
	Button_Teleport.Text = ""
	Button_Teleport.TextColor3 = Color3.new(0, 0, 0)
	Button_Teleport.TextSize = 14

	TextLabel.Parent = Teleport
	TextLabel.BackgroundColor3 = Color3.new(0, 0, 0)
	TextLabel.BackgroundTransparency = 0.5
	TextLabel.BorderColor3 = Color3.new(0, 0, 0)
	TextLabel.BorderSizePixel = 0
	TextLabel.Position = UDim2.new(-0.168098494, 0, -0.198757768, 0)
	TextLabel.Size = UDim2.new(0.943084836, 0, 0.200000003, 0)
	TextLabel.Font = Enum.Font.FredokaOne
	TextLabel.Text = "Teleport & AutoItme"
	TextLabel.TextColor3 = Color3.new(1, 1, 1)
	TextLabel.TextScaled = true
	TextLabel.TextSize = 14
	TextLabel.TextWrapped = true

	UICorner_2.Parent = TextLabel
	UICorner_2.CornerRadius = UDim.new(0, 5)

	local Stats = Instance.new("ImageLabel")
	local _1 = Instance.new("Frame")
	local UICorner_3 = Instance.new("UICorner")
	local _2 = Instance.new("Frame")
	local UICorner_4 = Instance.new("UICorner")
	local _2_2 = Instance.new("Frame")
	local UICorner_5 = Instance.new("UICorner")
	local Button_Stats = Instance.new("TextButton")
	local TextLabel_2 = Instance.new("TextLabel")
	Stats.Name = "Stats"
	Stats.Parent = Menu
	Stats.BackgroundColor3 = Color3.new(1, 1, 1)
	Stats.BackgroundTransparency = 1
	Stats.BorderColor3 = Color3.new(0, 0, 0)
	Stats.BorderSizePixel = 0
	Stats.Position = UDim2.new(0.632000089, 0, 0.0359999686, 0)
	Stats.Size = UDim2.new(0.5, 0, 0.467479676, 0)
	Stats.Image = "rbxassetid://14334760790"
	Stats.ImageColor3 = Color3.new(0.737255, 0.505882, 1)

	_1.Name = "1"
	_1.Parent = Stats
	_1.AnchorPoint = Vector2.new(0.5, 0.5)
	_1.BackgroundColor3 = Color3.new(1, 1, 1)
	_1.BorderColor3 = Color3.new(0, 0, 0)
	_1.BorderSizePixel = 0
	_1.Position = UDim2.new(0.5, 0, 0.544720471, 0)
	_1.Size = UDim2.new(0.115950756, 0, 0.45838508, 0)

	UICorner_3.Parent = _1

	_2.Name = "2"
	_2.Parent = Stats
	_2.AnchorPoint = Vector2.new(0.5, 0.5)
	_2.BackgroundColor3 = Color3.new(1, 1, 1)
	_2.BorderColor3 = Color3.new(0, 0, 0)
	_2.BorderSizePixel = 0
	_2.Position = UDim2.new(0.677437305, 0, 0.495031059, 0)
	_2.Size = UDim2.new(0.115950756, 0, 0.557763934, 0)

	UICorner_4.Parent = _2

	_2_2.Name = "2"
	_2_2.Parent = Stats
	_2_2.AnchorPoint = Vector2.new(0.5, 0.5)
	_2_2.BackgroundColor3 = Color3.new(1, 1, 1)
	_2_2.BorderColor3 = Color3.new(0, 0, 0)
	_2_2.BorderSizePixel = 0
	_2_2.Position = UDim2.new(0.319999993, 0, 0.574999988, 0)
	_2_2.Size = UDim2.new(0.115950756, 0, 0.383863986, 0)

	UICorner_5.Parent = _2_2

	Button_Stats.Name = "Button_Stats"
	Button_Stats.Parent = Stats
	Button_Stats.BackgroundColor3 = Color3.new(1, 1, 1)
	Button_Stats.BackgroundTransparency = 1
	Button_Stats.BorderColor3 = Color3.new(0, 0, 0)
	Button_Stats.BorderSizePixel = 0
	Button_Stats.Position = UDim2.new(0.100196317, 0, 0.224999994, 0)
	Button_Stats.Size = UDim2.new(0.767803609, 0, 0.550000012, 0)
	Button_Stats.Font = Enum.Font.SourceSans
	Button_Stats.Text = ""
	Button_Stats.TextColor3 = Color3.new(0, 0, 0)
	Button_Stats.TextSize = 14

	TextLabel_2.Parent = Stats
	TextLabel_2.BackgroundColor3 = Color3.new(0, 0, 0)
	TextLabel_2.BackgroundTransparency = 0.5
	TextLabel_2.BorderColor3 = Color3.new(0, 0, 0)
	TextLabel_2.BorderSizePixel = 0
	TextLabel_2.Position = UDim2.new(0.224131331, 0, -0.198757768, 0)
	TextLabel_2.Size = UDim2.new(0.943084836, 0, 0.200000003, 0)
	TextLabel_2.Font = Enum.Font.FredokaOne
	TextLabel_2.Text = "Stats"
	TextLabel_2.TextColor3 = Color3.new(1, 1, 1)
	TextLabel_2.TextScaled = true
	TextLabel_2.TextSize = 14
	TextLabel_2.TextWrapped = true

	local UICorner_6 = Instance.new("UICorner")
	UICorner_6.Parent = TextLabel_2
	UICorner_6.CornerRadius = UDim.new(0, 5)

	local Home = Instance.new("ImageLabel")
	local Icon_Home = Instance.new("ImageLabel")
	local Button_Home = Instance.new("TextButton")
	local TextLabel_3 = Instance.new("TextLabel")
	local UICorner_7 = Instance.new("UICorner")
	Home.Name = "Home"
	Home.Parent = Menu
	Home.BackgroundColor3 = Color3.new(1, 1, 1)
	Home.BackgroundTransparency = 1
	Home.BorderColor3 = Color3.new(0, 0, 0)
	Home.BorderSizePixel = 0
	Home.Position = UDim2.new(0.247999996, 0, -0.189999998, 0)
	Home.Size = UDim2.new(0.5, 0, 0.467479676, 0)
	Home.Image = "rbxassetid://14334760790"
	Home.ImageColor3 = Color3.new(1, 0.427451, 0.388235)

	Icon_Home.Name = "Icon_Home"
	Icon_Home.Parent = Home
	Icon_Home.AnchorPoint = Vector2.new(0.5, 0.5)
	Icon_Home.BackgroundColor3 = Color3.new(1, 1, 1)
	Icon_Home.BackgroundTransparency = 1
	Icon_Home.BorderColor3 = Color3.new(0, 0, 0)
	Icon_Home.BorderSizePixel = 0
	Icon_Home.Position = UDim2.new(0.5, 0, 0.5, 0)
	Icon_Home.Size = UDim2.new(0.550000012, 0, 0.550000012, 0)
	Icon_Home.Image = "rbxassetid://15169955786"

	Button_Home.Name = "Button_Home"
	Button_Home.Parent = Home
	Button_Home.BackgroundColor3 = Color3.new(1, 1, 1)
	Button_Home.BackgroundTransparency = 1
	Button_Home.BorderColor3 = Color3.new(0, 0, 0)
	Button_Home.BorderSizePixel = 0
	Button_Home.Position = UDim2.new(0.100196317, 0, 0.224999994, 0)
	Button_Home.Size = UDim2.new(0.767803609, 0, 0.550000012, 0)
	Button_Home.Font = Enum.Font.SourceSans
	Button_Home.Text = ""
	Button_Home.TextColor3 = Color3.new(0, 0, 0)
	Button_Home.TextSize = 14

	TextLabel_3.Parent = Home
	TextLabel_3.BackgroundColor3 = Color3.new(0, 0, 0)
	TextLabel_3.BackgroundTransparency = 0.5
	TextLabel_3.BorderColor3 = Color3.new(0, 0, 0)
	TextLabel_3.BorderSizePixel = 0
	TextLabel_3.Position = UDim2.new(0.0186776109, 0, -0.20869565, 0)
	TextLabel_3.Size = UDim2.new(0.943084836, 0, 0.200000003, 0)
	TextLabel_3.Font = Enum.Font.FredokaOne
	TextLabel_3.Text = "Home"
	TextLabel_3.TextColor3 = Color3.new(1, 1, 1)
	TextLabel_3.TextScaled = true
	TextLabel_3.TextSize = 14
	TextLabel_3.TextWrapped = true

	UICorner_7.Parent = TextLabel_3
	UICorner_7.CornerRadius = UDim.new(0, 5)

	local Shop = Instance.new("ImageLabel")
	local Icon_TP_2 = Instance.new("ImageLabel")
	local Button_Shop = Instance.new("TextButton")
	local TextLabel_4 = Instance.new("TextLabel")
	local UICorner_8 = Instance.new("UICorner")
	Shop.Name = "Shop"
	Shop.Parent = Menu
	Shop.BackgroundColor3 = Color3.new(1, 1, 1)
	Shop.BackgroundTransparency = 1
	Shop.BorderColor3 = Color3.new(0, 0, 0)
	Shop.BorderSizePixel = 0
	Shop.Position = UDim2.new(-0.140000001, 0, 0.500576019, 0)
	Shop.Size = UDim2.new(0.5, 0, 0.467479676, 0)
	Shop.Image = "rbxassetid://14334760790"
	Shop.ImageColor3 = Color3.new(0.294118, 1, 0.941177)

	Icon_TP_2.Name = "Icon_TP"
	Icon_TP_2.Parent = Shop
	Icon_TP_2.AnchorPoint = Vector2.new(0.5, 0.5)
	Icon_TP_2.BackgroundColor3 = Color3.new(1, 1, 1)
	Icon_TP_2.BackgroundTransparency = 1
	Icon_TP_2.BorderColor3 = Color3.new(0, 0, 0)
	Icon_TP_2.BorderSizePixel = 0
	Icon_TP_2.Position = UDim2.new(0.5, 0, 0.5, 0)
	Icon_TP_2.Size = UDim2.new(0.699999988, 0, 0.699999988, 0)
	Icon_TP_2.Image = "rbxassetid://6031265976"

	Button_Shop.Name = "Button_Shop"
	Button_Shop.Parent = Shop
	Button_Shop.BackgroundColor3 = Color3.new(1, 1, 1)
	Button_Shop.BackgroundTransparency = 1
	Button_Shop.BorderColor3 = Color3.new(0, 0, 0)
	Button_Shop.BorderSizePixel = 0
	Button_Shop.Position = UDim2.new(0.100196317, 0, 0.224999994, 0)
	Button_Shop.Size = UDim2.new(0.767803609, 0, 0.550000012, 0)
	Button_Shop.Font = Enum.Font.SourceSans
	Button_Shop.Text = ""
	Button_Shop.TextColor3 = Color3.new(0, 0, 0)
	Button_Shop.TextSize = 14

	TextLabel_4.Parent = Shop
	TextLabel_4.BackgroundColor3 = Color3.new(0, 0, 0)
	TextLabel_4.BackgroundTransparency = 0.5
	TextLabel_4.BorderColor3 = Color3.new(0, 0, 0)
	TextLabel_4.BorderSizePixel = 0
	TextLabel_4.Position = UDim2.new(-0.168098494, 0, 0.993788838, 0)
	TextLabel_4.Size = UDim2.new(0.943084836, 0, 0.200000003, 0)
	TextLabel_4.Font = Enum.Font.FredokaOne
	TextLabel_4.Text = "Shop"
	TextLabel_4.TextColor3 = Color3.new(1, 1, 1)
	TextLabel_4.TextScaled = true
	TextLabel_4.TextSize = 14
	TextLabel_4.TextWrapped = true

	UICorner_8.Parent = TextLabel_4
	UICorner_8.CornerRadius = UDim.new(0, 5)

	local Misc = Instance.new("ImageLabel")
	local Icon_TP_3 = Instance.new("ImageLabel")
	local Button_Misc = Instance.new("TextButton")
	local TextLabel_5 = Instance.new("TextLabel")
	local UICorner_9 = Instance.new("UICorner")
	Misc.Name = "Misc"
	Misc.Parent = Menu
	Misc.BackgroundColor3 = Color3.new(1, 1, 1)
	Misc.BackgroundTransparency = 1
	Misc.BorderColor3 = Color3.new(0, 0, 0)
	Misc.BorderSizePixel = 0
	Misc.Position = UDim2.new(0.630451441, 0, 0.500576019, 0)
	Misc.Size = UDim2.new(0.5, 0, 0.467479676, 0)
	Misc.Image = "rbxassetid://14334760790"
	Misc.ImageColor3 = Color3.new(1, 0.384314, 0.396078)

	Icon_TP_3.Name = "Icon_TP"
	Icon_TP_3.Parent = Misc
	Icon_TP_3.AnchorPoint = Vector2.new(0.5, 0.5)
	Icon_TP_3.BackgroundColor3 = Color3.new(1, 1, 1)
	Icon_TP_3.BackgroundTransparency = 1
	Icon_TP_3.BorderColor3 = Color3.new(0, 0, 0)
	Icon_TP_3.BorderSizePixel = 0
	Icon_TP_3.Position = UDim2.new(0.5, 0, 0.5, 0)
	Icon_TP_3.Size = UDim2.new(0.699999988, 0, 0.699999988, 0)
	Icon_TP_3.Image = "rbxassetid://6034509993"

	Button_Misc.Name = "Button_Misc"
	Button_Misc.Parent = Misc
	Button_Misc.BackgroundColor3 = Color3.new(1, 1, 1)
	Button_Misc.BackgroundTransparency = 1
	Button_Misc.BorderColor3 = Color3.new(0, 0, 0)
	Button_Misc.BorderSizePixel = 0
	Button_Misc.Position = UDim2.new(0.100196317, 0, 0.224999994, 0)
	Button_Misc.Size = UDim2.new(0.767803609, 0, 0.550000012, 0)
	Button_Misc.Font = Enum.Font.SourceSans
	Button_Misc.Text = ""
	Button_Misc.TextColor3 = Color3.new(0, 0, 0)
	Button_Misc.TextSize = 14

	TextLabel_5.Parent = Misc
	TextLabel_5.BackgroundColor3 = Color3.new(0, 0, 0)
	TextLabel_5.BackgroundTransparency = 0.5
	TextLabel_5.BorderColor3 = Color3.new(0, 0, 0)
	TextLabel_5.BorderSizePixel = 0
	TextLabel_5.Position = UDim2.new(0.224131331, 0, 0.993788838, 0)
	TextLabel_5.Size = UDim2.new(0.943084836, 0, 0.200000003, 0)
	TextLabel_5.Font = Enum.Font.FredokaOne
	TextLabel_5.Text = "Misc"
	TextLabel_5.TextColor3 = Color3.new(1, 1, 1)
	TextLabel_5.TextScaled = true
	TextLabel_5.TextSize = 14
	TextLabel_5.TextWrapped = true

	UICorner_9.Parent = TextLabel_5
	UICorner_9.CornerRadius = UDim.new(0, 5)

	local Out = Instance.new("ImageLabel")
	local Button_Out = Instance.new("TextButton")
	local Top = Instance.new("Frame")
	local UICorner_10 = Instance.new("UICorner")
	local Icon_Out = Instance.new("ImageLabel")

	Out.Name = "Out"
	Out.Parent = Menu
	Out.BackgroundColor3 = Color3.new(1, 1, 1)
	Out.BackgroundTransparency = 1
	Out.BorderColor3 = Color3.new(0, 0, 0)
	Out.BorderSizePixel = 0
	Out.Position = UDim2.new(0.247560427, 0, 0.728218317, 0)
	Out.Size = UDim2.new(0.5, 0, 0.467479676, 0)
	Out.Image = "rbxassetid://14334760790"
	Out.ImageColor3 = Color3.new(1, 1, 0.498039)

	Icon_Out.Name = "Icon_Out"
	Icon_Out.Parent = Out
	Icon_Out.AnchorPoint = Vector2.new(0.5, 0.5)
	Icon_Out.BackgroundColor3 = Color3.new(1, 1, 1)
	Icon_Out.BackgroundTransparency = 1
	Icon_Out.BorderColor3 = Color3.new(0, 0, 0)
	Icon_Out.BorderSizePixel = 0
	Icon_Out.Position = UDim2.new(0.5, 0, 0.5, 0)
	Icon_Out.Size = UDim2.new(0.699999988, 0, 0.699999988, 0)
	Icon_Out.Image = "rbxassetid://6023426922"

	Button_Out.Name = "Button_Out"
	Button_Out.Parent = Out
	Button_Out.BackgroundColor3 = Color3.new(1, 1, 1)
	Button_Out.BackgroundTransparency = 1
	Button_Out.BorderColor3 = Color3.new(0, 0, 0)
	Button_Out.BorderSizePixel = 0
	Button_Out.Position = UDim2.new(0.100196317, 0, 0.224999994, 0)
	Button_Out.Size = UDim2.new(0.767803609, 0, 0.550000012, 0)
	Button_Out.Font = Enum.Font.SourceSans
	Button_Out.Text = ""
	Button_Out.TextColor3 = Color3.new(0, 0, 0)
	Button_Out.TextSize = 14

	local ImageButton = Instance.new("ImageButton")
	local UICorner_16 = Instance.new("UICorner")
	ImageButton.Parent = QuarterlyHub
	ImageButton.BackgroundColor3 = Color3.new(0.164706, 0.164706, 0.164706)
	ImageButton.BackgroundTransparency = 0.5
	ImageButton.BorderColor3 = Color3.new(0, 0, 0)
	ImageButton.BorderSizePixel = 0
	ImageButton.Position = UDim2.new(0.0538812801, 0, 0.089430891, 0)
	ImageButton.Size = UDim2.new(0, 60, 0, 60)
	ImageButton.Visible = false
	ImageButton.Image = "rbxassetid://12781257228"

	UICorner_16.Parent = ImageButton

	local Bottom = Instance.new("Frame")
	Bottom.Name = "Bottom"
	Bottom.Parent = QuarterlyHub
	Bottom.AnchorPoint = Vector2.new(0.5, 0.5)
	Bottom.BackgroundColor3 = Color3.new(0.0666667, 0.0666667, 0.0666667)
	Bottom.BackgroundTransparency = 1
	Bottom.BorderColor3 = Color3.new(0, 0, 0)
	Bottom.BorderSizePixel = 0
	Bottom.Position = UDim2.new(0.5, 0, 0.5, 0)
	Bottom.Size = UDim2.new(0, 500, 0, 320)

	local UICorner_11 = Instance.new("UICorner")
	UICorner_11.Parent = Bottom

	local GUI = QuarterlyHub
	local UserInputService = game:GetService("UserInputService")
	local OpenUI = false
	local TweenService = game:GetService('TweenService')

	local OlyPos = {
		["Home"] = GUI.Menu.Home.Position,
		["Misc"] = GUI.Menu.Misc.Position,
		["Out"] = GUI.Menu.Out.Position,
		["Teleport"] = GUI.Menu.Teleport.Position,
		["Stats"] = GUI.Menu.Stats.Position,
		["Shop"] = GUI.Menu.Shop.Position,
	}

	local OlySize = {
		["Home"] = GUI.Menu.Home.Size,
		["Misc"] = GUI.Menu.Misc.Size,
		["Out"] = GUI.Menu.Out.Size,
		["Teleport"] = GUI.Menu.Teleport.Size,
		["Stats"] = GUI.Menu.Stats.Size,
		["Shop"] = GUI.Menu.Shop.Size,
	}

	local UIName = {
		"Home",
		"Misc",
		"Out",
		"Teleport",
		"Stats",
		"Shop",
	}

	for i, v in pairs(GUI.Menu:GetDescendants()) do
		if v.Name == "TextLabel" then
			v.BackgroundTransparency = 1
			v.TextTransparency = 1
		end
	end

	local PlayS = function()
		local Sound = Instance.new("Sound",workspace)
		Sound.PlaybackSpeed = 1.5
		Sound.Volume = 0.15
		Sound.SoundId = "rbxassetid://4601634016"
		Sound.PlayOnRemove = true
		Sound:Play()
		game.Debris:AddItem(Sound,1)
	end

	local SetPosUI = function()
		GUI.Menu.Size = UDim2.new(0,0,0,0)
		GUI.Menu.Rotation = 90
		for i, v in pairs(UIName) do
			GUI.Menu[v].Position = UDim2.new(.25,0,.27,0)
			GUI.Menu[v].Size = UDim2.new(0, 0, 0, 0) 
			GUI.Menu[v].Rotation = 160
		end
	end

	local SetPosUI2 = function()
		PlayS()
		for i, v in pairs(UIName) do
			TweenService:Create(
				GUI.Menu[v],
				TweenInfo.new(.5,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
				{Position = UDim2.new(.25,0,.27,0)}
			):Play()
			TweenService:Create(
				GUI.Menu[v],
				TweenInfo.new(.2,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
				{Rotation = 160}
			):Play()
		end
		wait(.3)
		for i, v in pairs(UIName) do
			TweenService:Create(
				GUI.Menu[v],
				TweenInfo.new(.2,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
				{Size = UDim2.new(0, 0, 0, 0)}
			):Play()
			TweenService:Create(
				GUI.Menu[v],
				TweenInfo.new(.5,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
				{Position = UDim2.new(.5,0,.5,0)}
			):Play()
			TweenService:Create(
				GUI.Menu[v],
				TweenInfo.new(.2,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
				{Rotation = 160}
			):Play()
		end
		wait(.3)
		TweenService:Create(
			GUI.Menu,
			TweenInfo.new(.5,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
			{Size = UDim2.new(0, 0, 0, 0)}
		):Play()
		TweenService:Create(
			GUI.Menu,
			TweenInfo.new(.2,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
			{Rotation = 90}
		):Play()
		wait(1)
		GUI.Enabled = false
		for i, v in pairs(UIName) do
			TweenService:Create(
				GUI.Menu[v],
				TweenInfo.new(.5,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
				{Position = UDim2.new(.25,0,.27,0)}
			):Play()
		end
	end

	UserInputService.InputBegan:Connect(function(input)
		if input.KeyCode == Enum.KeyCode.RightControl then
			PlayS()
			if OpenUI == true then
				SetPosUI2()
				OpenUI = false
			else
				SetPosUI()
				if GUI.Menu.Visible == false then
					GUI.Menu.Visible = true
				end
				GUI.Enabled = true
				TweenService:Create(
					GUI.Menu,
					TweenInfo.new(.2,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
					{Rotation = 0}
				):Play() 
				TweenService:Create(
					GUI.Menu,
					TweenInfo.new(.5,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
					{Size = UDim2.new(0, 150, 0, 150)}
				):Play()
				wait(1)
				for i, v in pairs(UIName) do
					TweenService:Create(
						GUI.Menu[v],
						TweenInfo.new(.2,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
						{Size = OlySize[v]}
					):Play() 
				end
				wait(.2)
				for i, v in pairs(UIName) do
					TweenService:Create(
						GUI.Menu[v],
						TweenInfo.new(.5,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
						{Position = OlyPos[v]}
					):Play()
				end
				for i, v in pairs(UIName) do
					TweenService:Create(
						GUI.Menu[v],
						TweenInfo.new(.2,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
						{Rotation = 0}
					):Play()
				end
				OpenUI = true
			end
		end
	end)

	GUI.Menu.Out.Button_Out.MouseButton1Click:Connect(function()
		SetPosUI2()
		GUI.Menu.Visible = false
		GUI.Enabled = true
		GUI.ImageButton.Visible = true
		GUI.ImageButton.MouseButton1Click:Connect(function()
			PlayS()
			GUI.ImageButton.Visible = false
			SetPosUI()
			if GUI.Menu.Visible == false then
				GUI.Menu.Visible = true
			end
			GUI.Enabled = true
			TweenService:Create(
				GUI.Menu,
				TweenInfo.new(.2,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
				{Rotation = 0}
			):Play() 
			TweenService:Create(
				GUI.Menu,
				TweenInfo.new(.5,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
				{Size = UDim2.new(0, 150, 0, 150)}
			):Play()
			wait(1)
			for i, v in pairs(UIName) do
				TweenService:Create(
					GUI.Menu[v],
					TweenInfo.new(.2,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
					{Size = OlySize[v]}
				):Play() 
			end
			wait(.3)
			for i, v in pairs(UIName) do
				TweenService:Create(
					GUI.Menu[v],
					TweenInfo.new(.5,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
					{Position = OlyPos[v]}
				):Play()
			end
			for i, v in pairs(UIName) do
				TweenService:Create(
					GUI.Menu[v],
					TweenInfo.new(.2,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
					{Rotation = 0}
				):Play()
			end
			OpenUI = true
		end)
	end)
	local tabs = {}
	function tabs:CreateTab(Name)
		for i,v in pairs(UIName) do
			if v == Name then
				local Main1 = Instance.new("Frame")
				Main1.Name = "Main1"
				Main1.Parent = Bottom
				Main1.AnchorPoint = Vector2.new(0.5, 0.5)
				Main1.BackgroundColor3 = Color3.new(0.0666667, 0.0666667, 0.0666667)
				Main1.BackgroundTransparency = 0
				Main1.BorderColor3 = Color3.new(17,17,17)
				Main1.BorderSizePixel = 0
				Main1.ClipsDescendants = true
				Main1.Position = UDim2.new(0.5, 0, 0.5, 0)
				Main1.Size = UDim2.new(0, 244, 0, 320)
				Main1.ZIndex = 1
				Main1.Visible = false

				local UIStroke = Instance.new("UIStroke")
				UIStroke.Color = _G.Color
				UIStroke.Thickness = 2
				UIStroke.Transparency = .2
				UIStroke.Name = "UIStroke"
				UIStroke.Parent = Main1

				local Main2 = Instance.new("Frame")
				local ImageButton_2 = Instance.new("ImageButton")
				Main2.Name = "Main2"
				Main2.Parent = Bottom
				Main2.BackgroundColor3 = _G.Color
				Main2.BorderColor3 = Color3.new(0, 0, 0)
				Main2.BorderSizePixel = 0
				Main2.Visible = false
				Main2.ZIndex = 2
				Main2.Position = UDim2.new(0.737999976, 0, 0, 0)
				Main2.Size = UDim2.new(0, 3, 0, 320)

				ImageButton_2.Parent = Main2
				ImageButton_2.BackgroundColor3 = Color3.new(1, 1, 1)
				ImageButton_2.BackgroundTransparency = 1
				ImageButton_2.BorderColor3 = Color3.new(0, 0, 0)
				ImageButton_2.BorderSizePixel = 0
				ImageButton_2.Position = UDim2.new(0, 0, 0.465999991, 0)
				ImageButton_2.Rotation = 180
				ImageButton_2.Size = UDim2.new(0, 22, 0, 22)
				ImageButton_2.Image = "rbxassetid://2777862332"

				local UICorner_12 = Instance.new("UICorner")
				UICorner_12.Parent = Main1
				UICorner_12.CornerRadius = UDim.new(0, 5)

				local Page = Instance.new("ScrollingFrame")
				local Left = Instance.new("ScrollingFrame")
				local Right = Instance.new("ScrollingFrame")
				local UIListLayout_5 = Instance.new("UIListLayout")
				local UIPadding_5 = Instance.new("UIPadding")

				Page.Name = "Page"
				Page.Parent = Main1
				Page.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
				Page.BackgroundTransparency = 1
				Page.Size = UDim2.new( 1, 0, 1, 0)
				Page.ScrollBarThickness = 0
				Page.ZIndex = 1
				Page.CanvasSize = UDim2.new(0, 0, 5, 0)
				Page.Visible = false

				Left.Name = "Left"
				Left.Parent = Page
				Left.Active = true
				Left.BackgroundColor3 = Color3.fromRGB(17, 17, 17)
				Left.BackgroundTransparency = 1
				Left.Size = UDim2.new(0, 245, 0, 335)
				Left.ScrollBarThickness = 0
				Left.CanvasSize = UDim2.new(0, 0, 0, 0)
				Left.ZIndex = -1

				Right.Name = "Right"
				Right.Parent = Page
				Right.Active = true
				Right.BackgroundColor3 = Color3.fromRGB(17, 17, 17)
				Right.BackgroundTransparency = 1
				Right.Size = UDim2.new(0, 245, 0, 335)
				Right.ScrollBarThickness = 0
				Right.CanvasSize = UDim2.new(0, 0, 0, 0)
				Right.ZIndex = -1

				local LeftList = Instance.new("UIListLayout")
				local RightList = Instance.new("UIListLayout")

				LeftList.Parent = Left
				LeftList.SortOrder = Enum.SortOrder.LayoutOrder
				LeftList.Padding = UDim.new(0, 5)

				RightList.Parent = Right
				RightList.SortOrder = Enum.SortOrder.LayoutOrder
				RightList.Padding = UDim.new(0, 5)


				ImageButton_2.MouseButton1Click:Connect(function()
					Main2.Visible = false
					TweenService:Create(
						Main1,
						TweenInfo.new(0.2,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
						{Size = UDim2.new(1, 0, 1, 0)}
					):Play()
					Page.Size = UDim2.new( 1, 0, 1, 0)
					Page.CanvasSize = UDim2.new(0, 0, 0, 0)
					UIListLayout_5.FillDirection = Enum.FillDirection.Horizontal
				end)

				UIListLayout_5.Parent = Page
				UIListLayout_5.FillDirection = Enum.FillDirection.Vertical 
				UIListLayout_5.SortOrder = Enum.SortOrder.LayoutOrder
				UIListLayout_5.Padding = UDim.new(0, 5)

				UIPadding_5.Parent = Page

				GUI.Menu[v]:FindFirstChildOfClass("TextLabel").Text = Name
				GUI.Menu[v]:FindFirstChildOfClass("TextButton").MouseEnter:Connect(function()
					if GUI.Menu[v]:FindFirstChildOfClass("ImageLabel") then
						GUI.Menu[v]:FindFirstChildOfClass("ImageLabel").ImageColor3 = Color3.fromRGB(57, 57, 57)
					else
						for _ii, _vv in pairs(GUI.Menu[v]:GetChildren()) do
							_vv.BackgroundColor3 = Color3.fromRGB(57, 57, 57)
						end
					end
					TweenService:Create(
						GUI.Menu[v]:FindFirstChildOfClass("TextLabel"),
						TweenInfo.new(.2,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
						{BackgroundTransparency = .5}
					):Play()
					TweenService:Create(
						GUI.Menu[v]:FindFirstChildOfClass("TextLabel"),
						TweenInfo.new(.2,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
						{TextTransparency = 0}
					):Play()
				end)
				GUI.Menu[v]:FindFirstChildOfClass("TextButton").MouseLeave:Connect(function()
					if GUI.Menu[v]:FindFirstChildOfClass("ImageLabel") then
						GUI.Menu[v]:FindFirstChildOfClass("ImageLabel").ImageColor3 = Color3.fromRGB(255, 255, 255)
					else
						for _ii, _vv in pairs(GUI.Menu[v]:GetChildren()) do
							_vv.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
						end
					end
					TweenService:Create(
						GUI.Menu[v]:FindFirstChildOfClass("TextLabel"),
						TweenInfo.new(.2,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
						{BackgroundTransparency = 1}
					):Play()
					TweenService:Create(
						GUI.Menu[v]:FindFirstChildOfClass("TextLabel"),
						TweenInfo.new(.2,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
						{TextTransparency = 1}
					):Play()
				end)
				GUI.Menu[v]:FindFirstChildOfClass("TextButton").MouseButton1Click:Connect(function()
					SetPosUI2()
					GUI.Menu.Visible = false
					GUI.Enabled = true

					if GUI.Menu[v]:FindFirstChildOfClass("ImageLabel") then
						GUI.Menu[v]:FindFirstChildOfClass("ImageLabel").ImageColor3 = Color3.fromRGB(255, 255, 255)
					else
						for _ii, _vv in pairs(GUI.Menu[v]:GetChildren()) do
							if _vv:FindFirstChildOfClass("Frame") then
								_vv.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
							end
						end
					end

					TweenService:Create(
						GUI.Menu[v]:FindFirstChildOfClass("TextLabel"),
						TweenInfo.new(.2,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
						{BackgroundTransparency = 1}
					):Play()
					TweenService:Create(
						GUI.Menu[v]:FindFirstChildOfClass("TextLabel"),
						TweenInfo.new(.2,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
						{TextTransparency = 1}
					):Play()
					local ImageButton = Instance.new("ImageButton")
					local UICorner_16 = Instance.new("UICorner")
					ImageButton.Parent = QuarterlyHub
					ImageButton.BackgroundColor3 = Color3.new(0.164706, 0.164706, 0.164706)
					ImageButton.BackgroundTransparency = 0.5
					ImageButton.BorderColor3 = Color3.new(0, 0, 0)
					ImageButton.BorderSizePixel = 0
					ImageButton.Position = UDim2.new(0.0538812801, 0, 0.089430891, 0)
					ImageButton.Size = UDim2.new(0, 60, 0, 60)
					ImageButton.Visible = false
					ImageButton.Image = "rbxassetid://6023426922"

					UICorner_16.Parent = ImageButton
					ImageButton.MouseButton1Click:Connect(function()
						PlayS()
						for  _i, _y in pairs(Main1:GetChildren()) do
							if _y:FindFirstChildOfClass("ScrollingFrame") then
								ImageButton:Destroy()
								TweenService:Create(
									_y,
									TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
									{Size = UDim2.new(0, 0, 0, 0)}
								):Play() 
								if GUI.Menu.Visible == false then
									GUI.Menu.Visible = true
									Main1.Visible = false
									Main2.Visible = false
									TweenService:Create(
										GUI.Menu,
										TweenInfo.new(.2,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
										{Rotation = 0}
									):Play() 
									TweenService:Create(
										GUI.Menu,
										TweenInfo.new(.5,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
										{Size = UDim2.new(0, 150, 0, 150)}
									):Play()
									wait(1)
									for i, v in pairs(UIName) do
										TweenService:Create(
											GUI.Menu[v],
											TweenInfo.new(.2,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
											{Size = OlySize[v]}
										):Play() 
									end
									wait(.5)
									for i, v in pairs(UIName) do
										TweenService:Create(
											GUI.Menu[v],
											TweenInfo.new(.5,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
											{Position = OlyPos[v]}
										):Play()
									end
									wait(.75)
									for i, v in pairs(UIName) do
										TweenService:Create(
											GUI.Menu[v],
											TweenInfo.new(.2,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
											{Rotation = 0}
										):Play()
									end
								end
								wait(.5)
								_y.Visible = false
							end
						end
					end)
					for  _i, _y in pairs(Main1:GetChildren()) do
						if _y:FindFirstChildOfClass("ScrollingFrame") then
							ImageButton.Visible = true
							_y.Size = UDim2.new( 0, 0, 0, 0)
							_y.Visible = false
						end
					end
					Main1.Visible = true

					UIListLayout_5.FillDirection = Enum.FillDirection.Vertical 
					Main1.Size = UDim2.new(0, 244, 0, 320)
					Main2.Visible = true
					Page.Visible = true
					TweenService:Create(
						Page,
						TweenInfo.new(.5,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
						{Size = UDim2.new(0, 275, 0, 335)}
					):Play() 
				end)

				local function GetType(value)
					if value == 1 or value == "Left" then
						return Left
					elseif value == 2 or value == "Right" then
						return Right
					else
						return Left
					end
				end

				game:GetService("RunService").Stepped:Connect(function()
					pcall(function()
						if Main2.Visible == true then
							Page.CanvasSize = UDim2.new( 0, 0, 5, 0)

							Right.CanvasSize = UDim2.new( 0, 0, 0, 0)
							Left.CanvasSize = UDim2.new( 0, 0, 0, 0)

							Left.Size = UDim2.new(0, 245, 0, LeftList.AbsoluteContentSize.Y + 30)
							Right.Size = UDim2.new(0, 245, 0, RightList.AbsoluteContentSize.Y + 30)
						else
							Left.Size = UDim2.new(0, 245, 0, 335)
							Right.Size = UDim2.new(0, 245, 0, 335)

							Right.CanvasSize = UDim2.new(0,0,0,RightList.AbsoluteContentSize.Y + 30)
							Left.CanvasSize = UDim2.new(0,0,0,LeftList.AbsoluteContentSize.Y + 30)

							Page.CanvasSize = UDim2.new(0, 0, 0, 0)
						end
					end)
				end)

				sections = {}
				function sections:CreateSection(options)
					local Name = options.Name
					local side = options.Side

					if side == nil then
						return Left
					end

					local Section = Instance.new("Frame")
					local UICorner_5 = Instance.new("UICorner")
					local Top_2 = Instance.new("Frame")
					local Line = Instance.new("Frame")
					local Sectionname = Instance.new("TextLabel")
					local SectionContainer = Instance.new("Frame")
					local SectionContainer_2 = Instance.new("Frame")
					local UIListLayout_2 = Instance.new("UIListLayout")
					local UIPadding_2 = Instance.new("UIPadding")

					Section.Name = "Section"
					Section.Parent = GetType(side)
					Section.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
					Section.ClipsDescendants = true
					Section.Transparency = 0.9
					Section.Size = UDim2.new(1, 0, 0, 120)

					local UICorner_Section = Instance.new("UICorner")
					UICorner_Section.Parent = Section

					Top_2.Name = "Top"
					Top_2.Parent = Section
					Top_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
					Top_2.BackgroundTransparency = 1.000
					Top_2.BorderColor3 = Color3.fromRGB(27, 42, 53)
					Top_2.Size = UDim2.new(1, 0, 0, 31)

	
					local Sectionname = Instance.new("TextLabel")
					Sectionname.Name = "Sectionname"
					Sectionname.Parent = Top_2
					Sectionname.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
					Sectionname.BackgroundTransparency = 1.000
					Sectionname.Position = UDim2.new(0.0591227226, 0, 0.0222222228, 0)
					Sectionname.Size = UDim2.new(0, 224, 0, 24)
					Sectionname.Font = Enum.Font.GothamBold
					Sectionname.Text = Name
					Sectionname.TextColor3 = Color3.fromRGB(255, 255, 255)
					Sectionname.TextSize = 10.000
					Sectionname.ZIndex = -1
					Sectionname.TextTransparency = 0
					Sectionname.TextXAlignment = Enum.TextXAlignment.Left

					SectionContainer.Name = "SectionContainer"
					SectionContainer.Parent = Top_2
					SectionContainer.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
					SectionContainer.BackgroundTransparency = 1.000
					SectionContainer.BorderSizePixel = 0
					SectionContainer.Position = UDim2.new(0, 0, 0.796416223, 0)
					SectionContainer.Size = UDim2.new(0, 239, 0, 270)

					SectionContainer_2.Name = "SectionContainer_2"
					SectionContainer_2.Parent = Top_2
					SectionContainer_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
					SectionContainer_2.BackgroundTransparency = 1.000
					SectionContainer_2.BorderSizePixel = 0
					SectionContainer_2.Position = UDim2.new(0, 0, 0.796416223, 0)
					SectionContainer_2.Size = UDim2.new(0, 239, 0, 270)

					UIListLayout_2.Parent = SectionContainer
					UIListLayout_2.SortOrder = Enum.SortOrder.LayoutOrder
					UIListLayout_2.Padding = UDim.new(0, 10)

					UIPadding_2.Parent = SectionContainer
					UIPadding_2.PaddingLeft = UDim.new(0, 5)

					UIListLayout_2:GetPropertyChangedSignal("AbsoluteContentSize"):Connect(function()
						Section.Size = UDim2.new(1, 0, 0, UIListLayout_2.AbsoluteContentSize.Y + 30)
					end)

					local functionitem = {}

					function functionitem:AddToggle(options)
						local Name = options.Name or ""
						local Flag = options.Flag or ""
						local default = options.Value
						local Mode = options.Mode or false
						local callback = options.Callback or function() end

						if Mode == false then
							local ToglFunc = {}
							local Tgo = default or false 
							local MainToggle = Instance.new("Frame")
							local UICorner = Instance.new("UICorner")
							local Text = Instance.new("TextLabel")
							local MainToggle_2 = Instance.new("ImageLabel")
							local UICorner_2 = Instance.new("UICorner")
							local MainToggle_3 = Instance.new("ImageLabel")
							local UICorner_3 = Instance.new("UICorner")
							local TextButton = Instance.new("TextButton")

							MainToggle.Name = Name
							MainToggle.Parent = SectionContainer
							MainToggle.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
							MainToggle.BackgroundTransparency = 1
							MainToggle.BorderSizePixel = 0
							MainToggle.ClipsDescendants = true
							MainToggle.Size = UDim2.new(1, 0, 0, 45)
							MainToggle.ZIndex = 16

							local UIStroke96 = Instance.new("UIStroke")
							UIStroke96.Thickness = 0.8
							UIStroke96.Parent = MainToggle
							UIStroke96.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
							UIStroke96.LineJoinMode = Enum.LineJoinMode.Round
							UIStroke96.Color = Color3.fromRGB(10, 11, 12)
							UIStroke96.Transparency = 0.3

							UICorner.CornerRadius = UDim.new(0, 4)
							UICorner.Parent = MainToggle

							Text.Name = "Text"
							Text.Parent = MainToggle
							Text.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
							Text.BackgroundTransparency = 1.000
							Text.Position = UDim2.new(0, 45, 0, 16)
							Text.Size = UDim2.new(0, 100, 0, 12)
							Text.ZIndex = 16
							Text.Font = Enum.Font.GothamBold
							Text.Text = Name
							Text.TextColor3 = Color3.fromRGB(255, 255, 255)
							Text.TextSize = 14.000
							Text.TextTransparency = 0.2
							Text.TextXAlignment = Enum.TextXAlignment.Left

							MainToggle_3.Name = "MainToggle"
							MainToggle_3.Parent = MainToggle
							MainToggle_3.AnchorPoint = Vector2.new(0.5, 0.5)
							MainToggle_3.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
							MainToggle_3.ClipsDescendants = true
							MainToggle_3.Position = UDim2.new(0, 20, 0.5, 0)
							MainToggle_3.Size = UDim2.new(0, 25, 0, 25)
							MainToggle_3.ZIndex = 16
							MainToggle_3.Image = "http://www.roblox.com/asset/?id="
							MainToggle_3.ImageColor3 = Color3.fromRGB(255, 255, 255)
							MainToggle_3.Visible = true

							UICorner_3.CornerRadius = UDim.new(0, 5)
							UICorner_3.Parent = MainToggle_3

							TextButton.Name = ""
							TextButton.Parent = MainToggle
							TextButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
							TextButton.BackgroundTransparency = 1.000
							TextButton.BorderSizePixel = 0
							TextButton.Position = UDim2.new(0, 0, 0, 0)
							TextButton.Size = UDim2.new(0, 265, 0, 35)
							TextButton.ZIndex = 16
							TextButton.AutoButtonColor = false
							TextButton.Font = Enum.Font.Gotham
							TextButton.Text = ""
							TextButton.TextColor3 = Color3.fromRGB(255, 255, 255)
							TextButton.TextSize = 14.000

							if default == true then
								pcall(callback,true)
								Tgo = true
								MainToggle_3.BackgroundColor3 = Color3.fromRGB(113, 255, 78)
								MainToggle_3:TweenSize(UDim2.new(0, 28, 0, 28),"In","Quad",0.2,true)
								MainToggle_3.Image = "http://www.roblox.com/asset/?id=6023426926"
								UICorner_3.CornerRadius = UDim.new(0, 100)
							end

							TextButton.MouseEnter:Connect(function()
								if Tgo == false then
									MainToggle_3.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
									MainToggle_3.Image = "http://www.roblox.com/asset/?id=00"
									MainToggle_3:TweenSize(UDim2.new(0, 28, 0, 28),"In","Quad",0.2,true)
									UICorner_3.CornerRadius = UDim.new(0, 5)
								else
									MainToggle_3.BackgroundColor3 = Color3.fromRGB(113, 255, 78)
									MainToggle_3:TweenSize(UDim2.new(0, 28, 0, 28),"In","Quad",0.2,true)
									MainToggle_3.Image = "http://www.roblox.com/asset/?id=6023426926"
									UICorner_3.CornerRadius = UDim.new(0, 100)
								end
							end)

							TextButton.MouseLeave:Connect(function()
								if Tgo == false then
									MainToggle_3.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
									MainToggle_3.Image = "http://www.roblox.com/asset/?id=00"
									MainToggle_3:TweenSize(UDim2.new(0, 25, 0, 25),"In","Quad",0.2,true)
									UICorner_3.CornerRadius = UDim.new(0, 5)
								else
									MainToggle_3.BackgroundColor3 = Color3.fromRGB(113, 255, 78)
									MainToggle_3:TweenSize(UDim2.new(0, 25, 0, 25),"In","Quad",0.2,true)
									MainToggle_3.Image = "http://www.roblox.com/asset/?id=6023426926"
									UICorner_3.CornerRadius = UDim.new(0, 100)
								end
							end)

							TextButton.MouseButton1Click:Connect(function()
								local SoundClick = Instance.new("Sound")
								SoundClick.Name = "SoundEffect"
								SoundClick.SoundId = "rbxassetid://130785805"
								SoundClick.Volume = 1
								SoundClick.Parent = game.Players.LocalPlayer.Character:WaitForChild("HumanoidRootPart")
								SoundClick:Play()
								if Tgo == false then
									Tgo = true
									pcall(callback,true)
									MainToggle_3.BackgroundColor3 = Color3.fromRGB(113, 255, 78)
									MainToggle_3.Image = "http://www.roblox.com/asset/?id=6023426926"
									UICorner_3.CornerRadius = UDim.new(0, 100)
									MainToggle_3:TweenSize(UDim2.new(0, 29, 0, 29),"In","Quad",0.2,true)
									wait(0.2)
									MainToggle_3:TweenSize(UDim2.new(0, 25, 0, 25),"In","Quad",0.2,true)
								else
									Tgo = false
									pcall(callback,false)
									MainToggle_3.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
									MainToggle_3.Image = "http://www.roblox.com/asset/?id=00"
									MainToggle_3:TweenSize(UDim2.new(0, 29, 0, 29),"In","Quad",0.2,true)
									UICorner_3.CornerRadius = UDim.new(0, 5)
									wait(0.2)
									MainToggle_3:TweenSize(UDim2.new(0, 25, 0, 25),"In","Quad",0.2,true)
								end
								wait(0.1)
								SoundClick:Destroy()
							end)
						else
							local ToglFunc = {}
							local Tgo = default or false
							local MainToggle = Instance.new("Frame")
							local UICorner = Instance.new("UICorner")
							local Text = Instance.new("TextLabel")
							local MainToggle_2 = Instance.new("ImageLabel")
							local UICorner_2 = Instance.new("UICorner")
							local MainToggle_3 = Instance.new("ImageLabel")
							local UICorner_3 = Instance.new("UICorner")
							local TextButton = Instance.new("TextButton")

							MainToggle.Name = "MainToggle"
							MainToggle.Parent = SectionContainer
							MainToggle.BackgroundColor3 = Color3.fromRGB(22, 22, 22)
							MainToggle.BackgroundTransparency = 0.2
							MainToggle.BorderSizePixel = 0
							MainToggle.ClipsDescendants = true
							MainToggle.Size = UDim2.new(1, 0, 0, 35)
							MainToggle.ZIndex = 16

							local UIStroke96 = Instance.new("UIStroke")
							UIStroke96.Thickness = 0.8
							UIStroke96.Parent = MainToggle
							UIStroke96.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
							UIStroke96.LineJoinMode = Enum.LineJoinMode.Round
							UIStroke96.Color = Color3.fromRGB(10, 11, 12)
							UIStroke96.Transparency = 0.3

							UICorner.CornerRadius = UDim.new(0, 4)
							UICorner.Parent = MainToggle

							Text.Name = "Text"
							Text.Parent = MainToggle
							Text.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
							Text.BackgroundTransparency = 1.000
							Text.Position = UDim2.new(0, 10, 0, 10)
							Text.Size = UDim2.new(0, 100, 0, 12)
							Text.ZIndex = 16
							Text.Font = Enum.Font.GothamBold
							Text.Text = Name
							Text.TextColor3 = Color3.fromRGB(255, 255, 255)
							Text.TextSize = 14.000
							Text.TextTransparency = 0
							Text.TextXAlignment = Enum.TextXAlignment.Left

							MainToggle_2.Name = "MainToggle"
							MainToggle_2.Parent = MainToggle
							MainToggle_2.AnchorPoint = Vector2.new(0.5, 0.5)
							MainToggle_2.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
							MainToggle_2.ClipsDescendants = true
							MainToggle_2.Position = UDim2.new(0, 200, 0.5, 0)
							MainToggle_2.Size = UDim2.new(0, 35, 0, 5)
							MainToggle_2.ZIndex = 16

							UICorner_2.CornerRadius = UDim.new(0, 3)
							UICorner_2.Parent = MainToggle_2

							MainToggle_3.Name = "MainToggle"
							MainToggle_3.Parent = MainToggle
							MainToggle_3.AnchorPoint = Vector2.new(0.5, 0.5)
							MainToggle_3.BackgroundColor3 = Color3.fromRGB(255, 0, 0)
							MainToggle_3.ClipsDescendants = true
							MainToggle_3.Position = UDim2.new(0, 185, 0.5, 0)
							MainToggle_3.Size = UDim2.new(0, 15, 0, 15)
							MainToggle_3.ZIndex = 16
							MainToggle_3.Image = "http://www.roblox.com/asset/?id="
							MainToggle_3.ImageColor3 = Color3.fromRGB(255, 0, 0)
							MainToggle_3.Visible = true
							UICorner_3.CornerRadius = UDim.new(0, 10)
							UICorner_3.Parent = MainToggle_3

							TextButton.Name = ""
							TextButton.Parent = MainToggle
							TextButton.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
							TextButton.BackgroundTransparency = 1.000
							TextButton.BorderSizePixel = 0
							TextButton.Size = UDim2.new(1, 0, 1, 0)
							TextButton.ZIndex = 16
							TextButton.AutoButtonColor = false
							TextButton.Font = Enum.Font.Gotham
							TextButton.Text = ""
							TextButton.TextColor3 = Color3.fromRGB(255, 255, 255)
							TextButton.TextSize = 14.000

							TextButton.MouseButton1Click:Connect(function()
								if Tgo == false then
									Tgo = true
									pcall(callback,true)
									MainToggle_3:TweenPosition(UDim2.new(0, 215, 0.5, 0),"In","Quad",0.1,true)
									MainToggle_3.BackgroundColor3 = Color3.fromRGB(0, 255, 0)
								else
									Tgo = false
									pcall(callback,false)
									MainToggle_3:TweenPosition(UDim2.new(0, 185, 0.5, 0),"In","Quad",0.1,true)
									MainToggle_3.BackgroundColor3 = Color3.fromRGB(255, 0, 0)
								end
							end)
							
							if default == true then
								Tgo = true
								pcall(callback,true)
								MainToggle_3:TweenPosition(UDim2.new(0, 215, 0.5, 0),"In","Quad",0.1,true)
								MainToggle_3.BackgroundColor3 = Color3.fromRGB(0, 255, 0)
							end
						end
					end

					function functionitem:AddLabelX(options)
						local text = options.Name
						local Flag = options.Flag
						local Mode = options.Mode
					
						local textas = {}
						local Label = Instance.new("Frame")
						local Text = Instance.new("TextLabel")
						Label.Name = text
						Label.Parent = SectionContainer
						Label.AnchorPoint = Vector2.new(0.5, 0.5)
						Label.BackgroundTransparency = 1.000
						Label.Size = UDim2.new( 1, 0, 0, 30)
	
						local Label22 = Instance.new("Frame")
						Label22.Name = "Label22"
						Label22.Parent = Label
						Label22.AnchorPoint = Vector2.new(0, 0.5)
						Label22.BackgroundColor3 = _G.Color
						Label22.Position = UDim2.new(0,0,0.5,0)
						Label22.Size = UDim2.new(0, 35, 0, 1)
	
						local Label23 = Instance.new("Frame")
						Label23.Name = "Label23"
						Label23.Parent = Label
						Label23.AnchorPoint = Vector2.new(0, 0.5)
						Label23.BackgroundColor3 = _G.Color
						Label23.Position = UDim2.new(0,195,0.5,0)
						Label23.Size = UDim2.new(0, 35, 0, 1)
	
						Text.Name = "Text"
						Text.Parent = Label
						Text.AnchorPoint = Vector2.new(0.5, 0.5)
						Text.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
						Text.BackgroundTransparency = 1.000
						Text.Position = UDim2.new(0.5, 0, 0.5, 0)
						Text.Size = UDim2.new(0, 53, 0, 150)
						Text.ZIndex = 16
						Text.Font = Enum.Font.GothamBold
						Text.Text = text
						Text.TextColor3 = Color3.fromRGB(255, 255, 255)
						Text.TextSize = 12.000
						function textas:Set(newtext)
							Text.Text = newtext
						end
						return textas
					end

					function functionitem:AddLabel(options)
						local text = options.Name
						local Flag = options.Flag
						local Mode = options.Mode
					
						local textas = {}
						local Label = Instance.new("Frame")
						local Text = Instance.new("TextLabel")
						Label.Name = text
						Label.Parent = SectionContainer
						Label.AnchorPoint = Vector2.new(0.5, 0.5)
						Label.BackgroundTransparency = 1.000
						Label.Size = UDim2.new( 1, 0, 0, 30)

						Text.Name = "Text"
						Text.Parent = Label
						Text.AnchorPoint = Vector2.new(0.5, 0.5)
						Text.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
						Text.BackgroundTransparency = 1.000
						Text.Position = UDim2.new(0.5, 0, 0.5, 0)
						Text.Size = UDim2.new(0, 53, 0, 150)
						Text.ZIndex = 16
						Text.Font = Enum.Font.GothamBold
						Text.Text = text
						Text.TextColor3 = Color3.fromRGB(255, 255, 255)
						Text.TextSize = 12.000
						function textas:Set(newtext)
							Text.Text = newtext
						end
						return textas
					end

					function functionitem:AddButton(options)
						local Name = options.Name or "Button"
						local callback = options.Callback or function() end
						local Mode = options.Mode or false

						if Mode == false then
							local Button = Instance.new("Frame")
							local UICorner_6 = Instance.new("UICorner")
							local TextLabel_3 = Instance.new("TextLabel")
							local TextButton = Instance.new("TextButton")
			
							Button.Name = "Button"
							Button.Parent = SectionContainer
							Button.BackgroundColor3 = Color3.fromRGB(22, 22, 22)
							Button.BackgroundTransparency = 0.2
							Button.Size = UDim2.new( 1, 0, 0, 30)
							Button.ZIndex = 16
			
							local UIStroke96 = Instance.new("UIStroke")
							UIStroke96.Thickness = 0.8
							UIStroke96.Parent = Button
							UIStroke96.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
							UIStroke96.LineJoinMode = Enum.LineJoinMode.Round
							UIStroke96.Color = Color3.fromRGB(10, 11, 12)
							UIStroke96.Transparency = 0.3

							UICorner_6.CornerRadius = UDim.new(0, 4)
							UICorner_6.Parent = Button
			
							TextLabel_3.Name = "Text"
							TextLabel_3.Parent = Button
							TextLabel_3.AnchorPoint = Vector2.new(0.5, 0.5)
							TextLabel_3.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
							TextLabel_3.BackgroundTransparency = 1.000
							TextLabel_3.Position = UDim2.new(0.5, 0, 0.5, 0)
							TextLabel_3.Size = UDim2.new(0, 100, 0, 12)
							TextLabel_3.ZIndex = 16
							TextLabel_3.Font = Enum.Font.GothamBold
							TextLabel_3.Text = Name
							TextLabel_3.TextColor3 = Color3.fromRGB(255, 255, 255)
							TextLabel_3.TextSize = 12.000
							TextLabel_3.TextTransparency = 0
			
							TextButton.Parent = Button
							TextButton.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
							TextButton.BackgroundTransparency = 1.000
							TextButton.BorderSizePixel = 0
							TextButton.ClipsDescendants = true
							TextButton.Size = UDim2.new(1, 0, 1, 0)
							TextButton.ZIndex = 16
							TextButton.AutoButtonColor = false
							TextButton.Font = Enum.Font.Gotham
							TextButton.Text = ""
							TextButton.TextColor3 = Color3.fromRGB(255, 255, 255)
							TextButton.TextSize = 14.000
							
							TextButton.MouseEnter:Connect(function()
								TweenService:Create(
									Button,
									TweenInfo.new(0.3,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
									{BackgroundTransparency = 0.5}
								):Play()
							end)
			
							TextButton.MouseLeave:Connect(function()
								TweenService:Create(
									Button,
									TweenInfo.new(0.3,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
									{BackgroundTransparency = 0}
								):Play()
							end)
			
							TextButton.MouseButton1Click:Connect(function()
								TextLabel_3.TextSize = 0
								TweenService:Create(
									TextLabel_3,
									TweenInfo.new(0.4,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
									{TextSize = 12}
								):Play()
								callback()
							end)
						else
							local Button = Instance.new("Frame")
							local UICorner_6 = Instance.new("UICorner")
							local TextLabel_3 = Instance.new("TextLabel")
							local TextButton = Instance.new("TextButton")
			
							Button.Name = "Button"
							Button.Parent = SectionContainer
							Button.BackgroundColor3 = Color3.fromRGB(22, 22, 22)
							Button.BackgroundTransparency = 1
							Button.Size = UDim2.new( 1, 0, 0, 30)
							Button.ZIndex = 16
			
							UICorner_6.CornerRadius = UDim.new(0, 4)
							UICorner_6.Parent = Button

							local Button2 = Instance.new("Frame")
							local UICorner_99 = Instance.new("UICorner")
							Button2.Name = "Button2"
							Button2.Parent = Button
							Button2.AnchorPoint = Vector2.new(0.5, 0.5)
							Button2.BackgroundColor3 = Color3.fromRGB(22, 22, 22)
							Button2.BackgroundTransparency = 0.2
							Button2.Size = UDim2.new( 0.8, 0, 0, 30)
							Button2.Position = UDim2.new(0.5, 0, 0.5, 0)
							Button2.ZIndex = 16

							local UIStroke96 = Instance.new("UIStroke")
							UIStroke96.Thickness = 0.8
							UIStroke96.Parent = Button2
							UIStroke96.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
							UIStroke96.LineJoinMode = Enum.LineJoinMode.Round
							UIStroke96.Color = Color3.fromRGB(10, 11, 12)
							UIStroke96.Transparency = 0.3
							
							UICorner_99.CornerRadius = UDim.new(0, 4)
							UICorner_99.Parent = Button2
			
							TextLabel_3.Name = "Text"
							TextLabel_3.Parent = Button2
							TextLabel_3.AnchorPoint = Vector2.new(0.5, 0.5)
							TextLabel_3.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
							TextLabel_3.BackgroundTransparency = 1.000
							TextLabel_3.Position = UDim2.new(0.5, 0, 0.5, 0)
							TextLabel_3.Size = UDim2.new(0, 100, 0, 12)
							TextLabel_3.ZIndex = 16
							TextLabel_3.Font = Enum.Font.GothamBold
							TextLabel_3.Text = Name
							TextLabel_3.TextColor3 = Color3.fromRGB(255, 255, 255)
							TextLabel_3.TextSize = 12.000
							TextLabel_3.TextTransparency = 0
			
							TextButton.Parent = Button
							TextButton.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
							TextButton.BackgroundTransparency = 1.000
							TextButton.BorderSizePixel = 0
							TextButton.ClipsDescendants = true
							TextButton.Size = UDim2.new(1, 0, 1, 0)
							TextButton.ZIndex = 16
							TextButton.AutoButtonColor = false
							TextButton.Font = Enum.Font.Gotham
							TextButton.Text = ""
							TextButton.TextColor3 = Color3.fromRGB(255, 255, 255)
							TextButton.TextSize = 14.000
							
							TextButton.MouseEnter:Connect(function()
								TweenService:Create(
									Button2,
									TweenInfo.new(0.3,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
									{BackgroundTransparency = 0.5}
								):Play()
							end)
			
							TextButton.MouseLeave:Connect(function()
								TweenService:Create(
									Button2,
									TweenInfo.new(0.3,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
									{BackgroundTransparency = 0}
								):Play()
							end)
			
							TextButton.MouseButton1Click:Connect(function()
								TextLabel_3.TextSize = 0
								TweenService:Create(
									TextLabel_3,
									TweenInfo.new(0.4,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
									{TextSize = 12}
								):Play()
								callback()
							end)
							
						end
					end

					function functionitem:AddDropdown(options)
						local text = options.Name
						local Flag = options.Flag
						local default = options.Value or ""
						local list = options.List
						local callback = options.Callback
		
						local Dropfunc = {}
		
						local MainDropDown = Instance.new("Frame")
						local UICorner_7 = Instance.new("UICorner")
						local MainDropDown_2 = Instance.new("Frame")
						local UICorner_8 = Instance.new("UICorner")
						local v = Instance.new("TextButton")
						local Text_2 = Instance.new("TextLabel")
						local ImageButton = Instance.new("ImageButton")
						local Scroll_Items = Instance.new("ScrollingFrame")
						local UIListLayout_3 = Instance.new("UIListLayout")
						local UIPadding_3 = Instance.new("UIPadding")
		
						local MainDropDown_3 = Instance.new("Frame")
						MainDropDown_3.Name = text
						MainDropDown_3.Parent = SectionContainer
						MainDropDown_3.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
						MainDropDown_3.Position = UDim2.new(0,0,2,0)
						MainDropDown_3.BackgroundTransparency = 1
						MainDropDown_3.BorderSizePixel = 0
						MainDropDown_3.ClipsDescendants = true
						MainDropDown_3.Size = UDim2.new(1, 0, 0, 15)
						MainDropDown_3.ZIndex = 16
		
						local Text_3 = Instance.new("TextLabel")
		
						Text_3.Name = "Text_3"
						Text_3.Parent = MainDropDown_3
						Text_3.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
						Text_3.BackgroundTransparency = 1.000
						Text_3.Size = UDim2.new(0, 62, 0, 12)
						Text_3.ZIndex = 16
						Text_3.Font = Enum.Font.GothamBold
						Text_3.Text = text
						Text_3.TextColor3 = Color3.fromRGB(255, 255, 255)
						Text_3.TextSize = 12.000
						Text_3.TextXAlignment = Enum.TextXAlignment.Left
		
						MainDropDown_2.Name = "MainDropDown"
						MainDropDown_2.Parent = MainDropDown
						MainDropDown_2.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
						MainDropDown_2.BackgroundTransparency = 0.700
						MainDropDown_2.BorderSizePixel = 0
						MainDropDown_2.ClipsDescendants = true
						MainDropDown_2.Size = UDim2.new(1, 0, 0, 35)
						MainDropDown_2.ZIndex = 16
		
						UICorner_8.CornerRadius = UDim.new(0, 4)
						UICorner_8.Parent = MainDropDown_2
		
						MainDropDown.Name = text
						MainDropDown.Parent = SectionContainer
						MainDropDown.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
						MainDropDown.BackgroundTransparency = 0.700
						MainDropDown.BorderSizePixel = 0
						MainDropDown.ClipsDescendants = true
						MainDropDown.Size = UDim2.new(1, 0, 0, 35)
						MainDropDown.ZIndex = 16
		
						local UIStroke96 = Instance.new("UIStroke")
						UIStroke96.Thickness = 1.2
						UIStroke96.Parent = MainDropDown
						UIStroke96.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
						UIStroke96.LineJoinMode = Enum.LineJoinMode.Round
						UIStroke96.Color = _G.Color
						UIStroke96.Transparency = 1
		
						MainDropDown.MouseEnter:Connect(function()
							TweenService:Create(
								UIStroke96,
								TweenInfo.new(0.4,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
								{Transparency = 0.10}
							):Play()
						end)
		
						MainDropDown.MouseLeave:Connect(function()
							TweenService:Create(
								UIStroke96,
								TweenInfo.new(0.4,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
								{Transparency = 1}
							):Play()
						end)
		
						UICorner_7.CornerRadius = UDim.new(0, 4)
						UICorner_7.Parent = MainDropDown
		
		
						v.Name = "v"
						v.Parent = MainDropDown_2
						v.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
						v.BackgroundTransparency = 1.000
						v.BorderSizePixel = 0
						v.Size = UDim2.new(1, 0, 1, 0)
						v.ZIndex = 16
						v.AutoButtonColor = false
						v.Font = Enum.Font.GothamBold
						v.Text = ""
						v.TextColor3 = Color3.fromRGB(255, 255, 255)
						v.TextSize = 12.000

						function getpro()
							if default then
								if table.find(list, default) then
									callback(default)
									return default
								else
									return ""
								end
							else
								return ""
							end
						end

						Text_2.Name = "Text"
						Text_2.Parent = MainDropDown
						Text_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
						Text_2.BackgroundTransparency = 1.000
						Text_2.Size = UDim2.new(1, 0, 0, 35)
						Text_2.ZIndex = 16
						Text_2.Font = Enum.Font.GothamBold
						Text_2.Text = getpro()
						Text_2.TextColor3 = Color3.fromRGB(255, 255, 255)
						Text_2.TextSize = 13.000
						Text_2.TextXAlignment = Enum.TextXAlignment.Center
		
						ImageButton.Parent = MainDropDown_2
						ImageButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
						ImageButton.BackgroundTransparency = 1
						ImageButton.Position = UDim2.new(0, 200, 0, 10)
						ImageButton.Size = UDim2.new(0, 13, 0, 13)
						ImageButton.ZIndex = 16
						ImageButton.Image = "http://www.roblox.com/asset/?id=6282522798"
		
						local UICorner_35 = Instance.new("UICorner")
						UICorner_35.CornerRadius = UDim.new(0, 5)
						UICorner_35.Parent = ImageButton
		
						Scroll_Items.Name = "Scroll_Items"
						Scroll_Items.Parent = MainDropDown
						Scroll_Items.Active = true
						Scroll_Items.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
						Scroll_Items.BackgroundTransparency = 1.000
						Scroll_Items.BorderSizePixel = 0
						Scroll_Items.Position = UDim2.new(0, 0, 0, 31)
						Scroll_Items.Size = UDim2.new(1, 0, 0, 375)
						Scroll_Items.CanvasSize = UDim2.new(0, 0, 0, 0)
						Scroll_Items.ScrollBarThickness = 0
	
						UIListLayout_3.Parent = Scroll_Items
						UIListLayout_3.SortOrder = Enum.SortOrder.LayoutOrder
						UIListLayout_3.Padding = UDim.new(0, 5)
						UIListLayout_3:GetPropertyChangedSignal("AbsoluteContentSize"):Connect(
						function()
							Scroll_Items.CanvasSize =  UDim2.new(0, 0, 0, UIListLayout_3.AbsoluteContentSize.Y*2)
						end)
						
						UIPadding_3.Parent = Scroll_Items
						UIPadding_3.PaddingLeft = UDim.new(0, 10)
						UIPadding_3.PaddingTop = UDim.new(0, 5)
		
						function Dropfunc:TogglePanel(state)
							TweenService:Create(
								MainDropDown,
								TweenInfo.new(.2, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
								{Size = state and UDim2.new(1, 0, 0, 299) or UDim2.new(1, 0, 0, 35)}
							):Play()
							TweenService:Create(
								ImageButton,
								TweenInfo.new(.2, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
								{Rotation = state and 180 or 0}
							):Play()
						end
						local Tof = false
						ImageButton.MouseButton1Click:Connect(
							function()
								Tof = not Tof
								Dropfunc:TogglePanel(Tof)
							end
						)
						v.MouseButton1Click:Connect(
							function()
								Tof = not Tof
								Dropfunc:TogglePanel(Tof)
							end
						)
						function Dropfunc:Clear()
							for i, v in next, Scroll_Items:GetChildren() do
								if v:IsA("TextButton") then 
									v:Destroy()
								end
							end
						end
		
						function Dropfunc:Add(Text)
							local _5 = Instance.new("TextButton")
							local UICorner_9 = Instance.new("UICorner")
							_5.Name = Text
							_5.Parent = Scroll_Items
							_5.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
							_5.BorderSizePixel = 0
							_5.ClipsDescendants = true
							_5.Size = UDim2.new(1, -10, 0, 30)
							_5.ZIndex = 17
							_5.AutoButtonColor = false
							_5.Font = Enum.Font.GothamBold
							_5.Text = Text
							_5.TextColor3 = Color3.fromRGB(255, 255, 255)
							_5.TextSize = 12.000
		
							UICorner_9.CornerRadius = UDim.new(0, 4)
							UICorner_9.Parent = _5
		
							local UIStroke96 = Instance.new("UIStroke")
							UIStroke96.Thickness = 1.2
							UIStroke96.Parent = _5
							UIStroke96.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
							UIStroke96.LineJoinMode = Enum.LineJoinMode.Round
							UIStroke96.Color = _G.Color
							UIStroke96.Transparency = 1
		
							for i, v in pairs(Scroll_Items:GetChildren()) do
								if v.Name == default then
									TweenService:Create(
										v,
										TweenInfo.new(.2, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
										{TextColor3 = Color3.fromRGB(0 , 200, 200)}
									):Play()
									callback(default)
								end
							end  
		
							_5.MouseEnter:Connect(function()
								TweenService:Create(
									UIStroke96,
									TweenInfo.new(0.4,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
									{Transparency = 0.10}
								):Play()
							end)
		
							_5.MouseLeave:Connect(function()
								TweenService:Create(
									UIStroke96,
									TweenInfo.new(0.4,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
									{Transparency = 1}
								):Play()
							end)
		
							_5.MouseButton1Click:Connect(
								function()
									if _x == nil then
										Tof = false
										TweenService:Create(
											_5,
											TweenInfo.new(.2, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
											{TextColor3 = Color3.fromRGB(0 , 200, 200)}
										):Play()
										Dropfunc:TogglePanel(Tof)
										callback(Text)
										Text_2.Text = Text
										_x = nil
									end
									for i, v in pairs(Scroll_Items:GetChildren()) do
										if v:IsA("TextButton") and v.TextColor3 == Color3.fromRGB(0, 200, 200) then
											TweenService:Create(
												v,
												TweenInfo.new(.2, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
												{TextColor3 = Color3.fromRGB(255, 255, 255)}
											):Play()
										end
									end
		
								end
							)
						end
						for i, v in next, list do
							Dropfunc:Add(v)
						end
						return Dropfunc
					end
					
					function functionitem:AddMultiDropdown(options)
						local text = options.Name
						local Flag = options.Flag
						local default = options.Value or {}
						local list = options.List
						local callback = options.Callback
	
						local Dropfunc = {}
	
						local MainDropDown = Instance.new("Frame")
						local UICorner_7 = Instance.new("UICorner")
						local MainDropDown_2 = Instance.new("Frame")
						local UICorner_8 = Instance.new("UICorner")
						local v = Instance.new("TextButton")
						local Text_2 = Instance.new("TextLabel")
						local ImageButton = Instance.new("ImageButton")
						local Scroll_Items = Instance.new("ScrollingFrame")
						local UIListLayout_3 = Instance.new("UIListLayout")
						local UIPadding_3 = Instance.new("UIPadding")
	
						local MainDropDown_3 = Instance.new("Frame")
	
						MainDropDown_3.Name = Name
						MainDropDown_3.Parent = SectionContainer
						MainDropDown_3.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
						MainDropDown_3.Position = UDim2.new(0,0,2,0)
						MainDropDown_3.BackgroundTransparency = 1
						MainDropDown_3.BorderSizePixel = 0
						MainDropDown_3.ClipsDescendants = true
						MainDropDown_3.Size = UDim2.new(1, 0, 0, 15)
						MainDropDown_3.ZIndex = 16
	
						local Text_3 = Instance.new("TextLabel")
	
						Text_3.Name = "Text_3"
						Text_3.Parent = MainDropDown_3
						Text_3.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
						Text_3.BackgroundTransparency = 1.000
						Text_3.Size = UDim2.new(0, 62, 0, 12)
						Text_3.ZIndex = 16
						Text_3.Font = Enum.Font.GothamBold
						Text_3.Text = Name
						Text_3.TextColor3 = Color3.fromRGB(255, 255, 255)
						Text_3.TextSize = 12.000
						Text_3.TextXAlignment = Enum.TextXAlignment.Left
	
						MainDropDown_2.Name = "MainDropDown"
						MainDropDown_2.Parent = MainDropDown
						MainDropDown_2.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
						MainDropDown_2.BackgroundTransparency = 0.700
						MainDropDown_2.BorderSizePixel = 0
						MainDropDown_2.ClipsDescendants = true
						MainDropDown_2.Size = UDim2.new(1, 0, 0, 35)
						MainDropDown_2.ZIndex = 16
	
						UICorner_8.CornerRadius = UDim.new(0, 4)
						UICorner_8.Parent = MainDropDown_2
	
						MainDropDown.Name = Name
						MainDropDown.Parent = SectionContainer
						MainDropDown.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
						MainDropDown.BackgroundTransparency = 0.700
						MainDropDown.BorderSizePixel = 0
						MainDropDown.ClipsDescendants = true
						MainDropDown.Size = UDim2.new(1, 0, 0, 35)
						MainDropDown.ZIndex = 16
	
						local UIStroke96 = Instance.new("UIStroke")
						UIStroke96.Thickness = 1.2
						UIStroke96.Parent = MainDropDown
						UIStroke96.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
						UIStroke96.LineJoinMode = Enum.LineJoinMode.Round
						UIStroke96.Color = _G.Color
						UIStroke96.Transparency = 1
	
						MainDropDown.MouseEnter:Connect(function()
							TweenService:Create(
								UIStroke96,
								TweenInfo.new(0.4,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
								{Transparency = 0.10}
							):Play()
						end)
	
						MainDropDown.MouseLeave:Connect(function()
							TweenService:Create(
								UIStroke96,
								TweenInfo.new(0.4,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
								{Transparency = 1}
							):Play()
						end)
	
						UICorner_7.CornerRadius = UDim.new(0, 4)
						UICorner_7.Parent = MainDropDown
	
						v.Name = "v"
						v.Parent = MainDropDown_2
						v.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
						v.BackgroundTransparency = 1.000
						v.BorderSizePixel = 0
						v.Size = UDim2.new(1, 0, 1, 0)
						v.ZIndex = 16
						v.AutoButtonColor = false
						v.Font = Enum.Font.GothamBold
						v.Text = ""
						v.TextColor3 = Color3.fromRGB(255, 255, 255)
						v.TextSize = 12.000
						function getpro()
							if default then
								for i, v in next, default do
									if table.find(list, v) then
										callback(default)
									end
								end
							end
						end
	
						Text_2.Name = "Text"
						Text_2.Parent = MainDropDown_2
						Text_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
						Text_2.BackgroundTransparency = 1.000
						Text_2.Size = UDim2.new(1, 0, 0, 35)
						Text_2.ZIndex = 16
						Text_2.Font = Enum.Font.GothamBold
						Text_2.Text = table.concat(default, ", ")
						Text_2.TextColor3 = Color3.fromRGB(255, 255, 255)
						Text_2.TextSize = 13.000
						Text_2.TextXAlignment = Enum.TextXAlignment.Center
	
						ImageButton.Parent = MainDropDown_2
						ImageButton.AnchorPoint = Vector2.new(0, 0.5)
						ImageButton.BackgroundTransparency = 1.000
						ImageButton.Position = UDim2.new(1, -25, 0.5, 0)
						ImageButton.Size = UDim2.new(0, 12, 0, 12)
						ImageButton.ZIndex = 16
						ImageButton.Image = "http://www.roblox.com/asset/?id=6282522798"
						local DropTable = {}
						Scroll_Items.Name = "Scroll_Items"
						Scroll_Items.Parent = MainDropDown
						Scroll_Items.Active = true
						Scroll_Items.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
						Scroll_Items.BackgroundTransparency = 1.000
						Scroll_Items.BorderSizePixel = 0
						Scroll_Items.Position = UDim2.new(0, 0, 0, 35)
						Scroll_Items.Size = UDim2.new(1, 0, 1, -35)
						Scroll_Items.ZIndex = 16
						Scroll_Items.CanvasSize = UDim2.new(0, 0, 0, 265)
						Scroll_Items.ScrollBarThickness = 0
	
						UIListLayout_3.Parent = Scroll_Items
						UIListLayout_3.SortOrder = Enum.SortOrder.LayoutOrder
						UIListLayout_3.Padding = UDim.new(0, 5)
						UIListLayout_2:GetPropertyChangedSignal("AbsoluteContentSize"):Connect(
						function()
							Scroll_Items.CanvasSize = UDim2.new(1, 0, 0, UIListLayout_2.AbsoluteContentSize.Y+40)
						end
						)
						UIPadding_3.Parent = Scroll_Items
						UIPadding_3.PaddingLeft = UDim.new(0, 10)
						UIPadding_3.PaddingTop = UDim.new(0, 5)
	
						function Dropfunc:TogglePanel(state)
							TweenService:Create(
								MainDropDown,
								TweenInfo.new(.2, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
								{Size = state and UDim2.new(1, 0, 0, 200) or UDim2.new(1, 0, 0, 35)}
							):Play()
							TweenService:Create(
								ImageButton,
								TweenInfo.new(.2, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
								{Rotation = state and 180 or 0}
							):Play()
						end
						local Tof = false
						ImageButton.MouseButton1Click:Connect(
							function()
								Tof = not Tof
								Dropfunc:TogglePanel(Tof)
							end
						)
						v.MouseButton1Click:Connect(
							function()
								Tof = not Tof
								Dropfunc:TogglePanel(Tof)
							end
						)

						function Dropfunc:Add(Text)
							local _5 = Instance.new("TextButton")
							local UICorner_9 = Instance.new("UICorner")
							_5.Name = Text
							_5.Parent = Scroll_Items
							_5.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
							_5.BorderSizePixel = 0
							_5.ClipsDescendants = true
							_5.Size = UDim2.new(1, -10, 0, 30)
							_5.ZIndex = 17
							_5.AutoButtonColor = false
							_5.Font = Enum.Font.GothamBold
							_5.Text = Text
							_5.TextColor3 = Color3.fromRGB(255, 255, 255)
							_5.TextSize = 12.000
	
							local UIStroke96 = Instance.new("UIStroke")
							UIStroke96.Thickness = 1.2
							UIStroke96.Parent = _5
							UIStroke96.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
							UIStroke96.LineJoinMode = Enum.LineJoinMode.Round
							UIStroke96.Color = _G.Color
							UIStroke96.Transparency = 1
	
							_5.MouseEnter:Connect(function()
								TweenService:Create(
									UIStroke96,
									TweenInfo.new(0.4,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
									{Transparency = 0.10}
								):Play()
							end)
	
							_5.MouseLeave:Connect(function()
								TweenService:Create(
									UIStroke96,
									TweenInfo.new(0.4,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
									{Transparency = 1}
								):Play()
							end)
	
							UICorner_9.CornerRadius = UDim.new(0, 4)
							UICorner_9.Parent = _5
							_5.MouseButton1Click:Connect(
								function()
									if not table.find(DropTable, Text) then
										table.insert(DropTable, Text)
										callback(DropTable, Text)
										Text_2.Text = table.concat(DropTable, ", ")
										TweenService:Create(
											_5,
											TweenInfo.new(.2, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
											{TextColor3 = _G.Color}
										):Play()
									else
										TweenService:Create(
											_5,
											TweenInfo.new(.2, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
											{TextColor3 = Color3.fromRGB(255, 255, 255)}
										):Play()
										for i2, v2 in pairs(DropTable) do
											if v2 == Text then
												table.remove(DropTable, i2)
												Text_2.Text = table.concat(DropTable, ", ")
											end
										end
										callback(DropTable, Text)
									end
								end
							)
						end
						function Dropfunc:Clear()
							for i, v in next, Scroll_Items:GetChildren() do
								if v:IsA("TextButton")  then 
									v:Destroy()
								end
							end 
						end
	
						for i, v in next, list do
							Dropfunc:Add(v)
						end
						return Dropfunc
					end
	
					function functionitem:AddSlider(options)
						--text,floor,min,max,de,callback
						local text = options.Name
						local floor = options.floor or false
						local Flag = options.Flag
						local de = options.Value or 1
						local min = options.Min or 1
						local max = options.Max or 2
	
						local callback = options.Format or function() end
	
						local SliderFrame = Instance.new("Frame")
						local LabelNameSlider = Instance.new("TextLabel")
						local ShowValueFrame = Instance.new("Frame")
						local CustomValue = Instance.new("TextBox")
						local ShowValueFrameUICorner = Instance.new("UICorner")
						local ValueFrame = Instance.new("Frame")
						local ValueFrameUICorner = Instance.new("UICorner")
						local PartValue = Instance.new("Frame")
						local PartValueUICorner = Instance.new("UICorner")
						local MainValue = Instance.new("Frame")
						local MainValueUICorner = Instance.new("UICorner")
						local sliderfunc = {}
	
						SliderFrame.Name = text
						SliderFrame.Parent = SectionContainer
						SliderFrame.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
						SliderFrame.BackgroundTransparency = 0.700
						SliderFrame.Position = UDim2.new(0.109489053, 0, 0.708609283, 0)
						SliderFrame.Size = UDim2.new(1, 0, 0, 45)
	
						local UIStroke96 = Instance.new("UIStroke")
						UIStroke96.Thickness = 1.2
						UIStroke96.Parent = SliderFrame
						UIStroke96.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
						UIStroke96.LineJoinMode = Enum.LineJoinMode.Round
						UIStroke96.Color = _G.Color
						UIStroke96.Transparency = 1
	
						SliderFrame.MouseEnter:Connect(function()
							TweenService:Create(
								UIStroke96,
								TweenInfo.new(0.4,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
								{Transparency = 0.10}
							):Play()
						end)
	
						SliderFrame.MouseLeave:Connect(function()
							TweenService:Create(
								UIStroke96,
								TweenInfo.new(0.4,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
								{Transparency = 1}
							):Play()
						end)
	
						local UICorner_7 = Instance.new("UICorner")
						UICorner_7.CornerRadius = UDim.new(0, 4)
						UICorner_7.Parent = SliderFrame
	
						LabelNameSlider.Name = "LabelNameSlider"
						LabelNameSlider.Parent = SliderFrame
						LabelNameSlider.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
						LabelNameSlider.BackgroundTransparency = 1.000
						LabelNameSlider.Position = UDim2.new(0.0729926974, 0, 0.0396823473, 0)
						LabelNameSlider.Size = UDim2.new(0, 182, 0, 25)
						LabelNameSlider.Font = Enum.Font.GothamBold
						LabelNameSlider.Text = tostring(text)
						LabelNameSlider.TextColor3 = Color3.fromRGB(255, 255, 255)
						LabelNameSlider.TextSize = 11.000
						LabelNameSlider.TextXAlignment = Enum.TextXAlignment.Left
	
						ShowValueFrame.Name = "ShowValueFrame"
						ShowValueFrame.Parent = SliderFrame
						ShowValueFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
						ShowValueFrame.Position = UDim2.new(0.733576655, 0, 0.0656082779, 0)
						ShowValueFrame.Size = UDim2.new(0, 58, 0, 21)
	
						CustomValue.Name = "CustomValue"
						CustomValue.Parent = ShowValueFrame
						CustomValue.AnchorPoint = Vector2.new(0.5, 0.5)
						CustomValue.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
						CustomValue.Position = UDim2.new(0.5, 0, 0.5, 0)
						CustomValue.Size = UDim2.new(0, 55, 0, 21)
						CustomValue.Font = Enum.Font.GothamBold
						CustomValue.Text = ""
						CustomValue.TextColor3 = Color3.fromRGB(255, 255, 255)
						CustomValue.TextSize = 11.000
	
						local UIStroke965 = Instance.new("UIStroke")
						UIStroke965.Thickness = 1.2
						UIStroke965.Parent = CustomValue
						UIStroke965.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
						UIStroke965.LineJoinMode = Enum.LineJoinMode.Round
						UIStroke965.Color = _G.Color
						UIStroke965.Transparency = 0.10
	
						SliderFrame.MouseEnter:Connect(function()
							TweenService:Create(
								UIStroke965,
								TweenInfo.new(0.4,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
								{Transparency = 0.5}
							):Play()
						end)
	
						SliderFrame.MouseLeave:Connect(function()
							TweenService:Create(
								UIStroke965,
								TweenInfo.new(0.4,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
								{Transparency = 0.10}
							):Play()
						end)
	
						ShowValueFrameUICorner.CornerRadius = UDim.new(0, 4)
						ShowValueFrameUICorner.Name = "ShowValueFrameUICorner"
						ShowValueFrameUICorner.Parent = ShowValueFrame
	
						ValueFrame.Name = "ValueFrame"
						ValueFrame.Parent = SliderFrame
						ValueFrame.AnchorPoint = Vector2.new(0.5, 0.5)
						ValueFrame.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
						ValueFrame.Position = UDim2.new(0.5, 0, 0.8, 0)
						ValueFrame.Size = UDim2.new(0, 185, 0, 5)
	
						ValueFrameUICorner.CornerRadius = UDim.new(0, 30)
						ValueFrameUICorner.Name = "ValueFrameUICorner"
						ValueFrameUICorner.Parent = ValueFrame
	
						PartValue.Name = "PartValue"
						PartValue.Parent = ValueFrame
						PartValue.AnchorPoint = Vector2.new(0.5, 0.5)
						PartValue.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
						PartValue.BackgroundTransparency = 1.000
						PartValue.Position = UDim2.new(0.5, 0, 0.8, 0)
						PartValue.Size = UDim2.new(0, 185, 0, 5)
	
						PartValueUICorner.CornerRadius = UDim.new(0, 30)
						PartValueUICorner.Name = "PartValueUICorner"
						PartValueUICorner.Parent = PartValue
	
						MainValue.Name = "MainValue"
						MainValue.Parent = ValueFrame
						MainValue.BackgroundColor3 = _G.Color
						MainValue.Size = UDim2.new((de or 0) / max, 0, 0, 5)
						MainValue.BorderSizePixel = 0
	
						MainValueUICorner.CornerRadius = UDim.new(0, 30)
						MainValueUICorner.Name = "MainValueUICorner"
						MainValueUICorner.Parent = MainValue
	
	
						local ConneValue = Instance.new("Frame")
						ConneValue.Name = "ConneValue"
						ConneValue.Parent = PartValue
						ConneValue.AnchorPoint = Vector2.new(0.7, 0.7)
						ConneValue.BackgroundColor3 = _G.Color
						ConneValue.Position = UDim2.new((de or 0)/max, 0.5, 0.5,0, 0)
						ConneValue.Size = UDim2.new(0, 10, 0, 10)
						ConneValue.BorderSizePixel = 0
	
						local UICorner = Instance.new("UICorner")
						UICorner.CornerRadius = UDim.new(0, 10)
						UICorner.Parent = ConneValue
	
	
						if floor == true then
							CustomValue.Text =  tostring(de and string.format("%0.2f",(de / max) * (max - min) + min) or 0)
						else
							CustomValue.Text =  tostring(de and math.floor((de / max) * (max - min) + min) or 0)
						end
	
						local function move(input)
							local pos =
								UDim2.new(
									math.clamp((input.Position.X - ValueFrame.AbsolutePosition.X) / ValueFrame.AbsoluteSize.X, 0, 1),
									0,
									0.5,
									0
								)
							local pos1 =
								UDim2.new(
									math.clamp((input.Position.X - ValueFrame.AbsolutePosition.X) / ValueFrame.AbsoluteSize.X, 0, 1),
									0,
									0,
									5
								)
							MainValue:TweenSize(pos1, "Out", "Sine", 0.2, true)
							ConneValue:TweenPosition(pos, "Out", "Sine", 0.2, true)
							if floor == true then
								local value = string.format("%.0f",((pos.X.Scale * max) / max) * (max - min) + min)
								CustomValue.Text = tostring(value)
								callback(value)
							else
								local value = math.floor(((pos.X.Scale * max) / max) * (max - min) + min)
								CustomValue.Text = tostring(value)
								callback(value)
							end
						end
						local dragging = false
						ConneValue.InputBegan:Connect(
							function(input)
								if input.UserInputType == Enum.UserInputType.MouseButton1 then
									dragging = true
								end
							end)
						ConneValue.InputEnded:Connect(
							function(input)
								if input.UserInputType == Enum.UserInputType.MouseButton1 then
									dragging = false
								end
							end)
						SliderFrame.InputBegan:Connect(
							function(input)
								if input.UserInputType == Enum.UserInputType.MouseButton1 then
									dragging = true
								end
							end)
						SliderFrame.InputEnded:Connect(
							function(input)
								if input.UserInputType == Enum.UserInputType.MouseButton1 then
									dragging = false
								end
							end)
						ValueFrame.InputBegan:Connect(
							function(input)
								if input.UserInputType == Enum.UserInputType.MouseButton1 then
									dragging = true
								end
							end)
						ValueFrame.InputEnded:Connect(
							function(input)
								if input.UserInputType == Enum.UserInputType.MouseButton1 then
									dragging = false
								end
							end)
						game:GetService("UserInputService").InputChanged:Connect(function(input)
							if dragging and input.UserInputType == Enum.UserInputType.MouseMovement then
								move(input)
							end
						end)
						CustomValue.FocusLost:Connect(function()
							if CustomValue.Text == "" then
								CustomValue.Text  = de
							end
							if  tonumber(CustomValue.Text) > max then
								CustomValue.Text  = max
							end
							MainValue:TweenSize(UDim2.new((CustomValue.Text or 0) / max, 0, 0, 5), "Out", "Sine", 0.2, true)
							ConneValue:TweenPosition(UDim2.new((CustomValue.Text or 0)/max, 0,0.6, 0) , "Out", "Sine", 0.2, true)
							if floor == true then
								CustomValue.Text = tostring(CustomValue.Text and string.format("%.0f",(CustomValue.Text / max) * (max - min) + min) )
							else
								CustomValue.Text = tostring(CustomValue.Text and math.floor( (CustomValue.Text / max) * (max - min) + min) )
							end
							pcall(callback, CustomValue.Text)
						end)
	
						function sliderfunc:Update(value)
							MainValue:TweenSize(UDim2.new((value or 0) / max, 0, 0, 5), "Out", "Sine", 0.2, true)
							ConneValue:TweenPosition(UDim2.new((value or 0)/max, 0.5, 0.5,0, 0) , "Out", "Sine", 0.2, true)
							CustomValue.Text = value
							pcall(function()
								callback(value)
							end)
						end
						return sliderfunc
					end

					function functionitem:AddColorpicker(text, preset, callback)
						local OldToggleColor = Color3.fromRGB(0, 0, 0)
						local OldColor = Color3.fromRGB(0, 0, 0)
						local OldColorSelectionPosition = nil
						local OldHueSelectionPosition = nil
						local ColorH, ColorS, ColorV = 1, 1, 1
						local RainbowColorPicker = false
						local ColorPickerInput = nil
						local ColorInput = nil
						local HueInput = nil
	
						local Colorpicker = Instance.new("Frame")
						local ColorpickerTitle = Instance.new("TextLabel")
						local ColorpickerFrameOutline = Instance.new("Frame")
						local ColorpickerFrameOutlineCorner = Instance.new("UICorner")
						local ColorpickerFrame = Instance.new("Frame")
						local ColorpickerFrameCorner = Instance.new("UICorner")
						local Color = Instance.new("ImageLabel")
						local ColorCorner = Instance.new("UICorner")
						local ColorSelection = Instance.new("ImageLabel")
						local Hue = Instance.new("ImageLabel")
						local HueCorner = Instance.new("UICorner")
						local HueGradient = Instance.new("UIGradient")
						local HueSelection = Instance.new("ImageLabel")
						local PresetClr = Instance.new("Frame")
						local PresetClrCorner = Instance.new("UICorner")
	
						Colorpicker.Name = "Colorpicker"
						Colorpicker.Parent = SectionContainer
						Colorpicker.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
						Colorpicker.BackgroundTransparency = 1.000
						Colorpicker.Position = UDim2.new(0.0895741582, 0, 0.474232763, 0)
						Colorpicker.Size = UDim2.new(1, 0, 0, 175)
	
						ColorpickerTitle.Name = "ColorpickerTitle"
						ColorpickerTitle.Parent = Colorpicker
						ColorpickerTitle.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
						ColorpickerTitle.BackgroundTransparency = 1.000
						ColorpickerTitle.Position = UDim2.new(0, 5, 0, 0)
						ColorpickerTitle.Size = UDim2.new(.92, 0, 0, 29)
						ColorpickerTitle.Font = Enum.Font.Gotham
						ColorpickerTitle.Text = "Colorpicker"
						ColorpickerTitle.TextColor3 = Color3.fromRGB(255, 255, 255)
						ColorpickerTitle.TextSize = 14.000
						ColorpickerTitle.TextXAlignment = Enum.TextXAlignment.Left
	
						ColorpickerFrameOutline.Name = "ColorpickerFrameOutline"
						ColorpickerFrameOutline.Parent = ColorpickerTitle
						ColorpickerFrameOutline.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
						ColorpickerFrameOutline.Position = UDim2.new(-0.00100000005, 0, 0.991999984, 0)
						ColorpickerFrameOutline.Size = UDim2.new(1.025, 0, 0, 139)
	
						ColorpickerFrameOutlineCorner.CornerRadius = UDim.new(0, 3)
						ColorpickerFrameOutlineCorner.Name = "ColorpickerFrameOutlineCorner"
						ColorpickerFrameOutlineCorner.Parent = ColorpickerFrameOutline
	
						ColorpickerFrame.Name = "ColorpickerFrame"
						ColorpickerFrame.Parent = ColorpickerTitle
						ColorpickerFrame.BackgroundColor3 = Color3.fromRGB(23, 23, 23)
						ColorpickerFrame.ClipsDescendants = true
						ColorpickerFrame.Position = UDim2.new(0.00899999978, 0, 1.06638515, 0)
						ColorpickerFrame.Selectable = true
						ColorpickerFrame.Size = UDim2.new(1, 0, 0, 135)
	
						ColorpickerFrameCorner.CornerRadius = UDim.new(0, 3)
						ColorpickerFrameCorner.Name = "ColorpickerFrameCorner"
						ColorpickerFrameCorner.Parent = ColorpickerFrame
	
						Color.Name = "Color"
						Color.Parent = ColorpickerFrame
						Color.BackgroundColor3 = Color3.fromRGB(255, 0, 4)
						Color.Position = UDim2.new(0, 10, 0, 10)
						Color.Size = UDim2.new(0, 154, 0, 118)
						Color.ZIndex = 10
						Color.Image = "rbxassetid://4155801252"
	
						ColorCorner.CornerRadius = UDim.new(0, 3)
						ColorCorner.Name = "ColorCorner"
						ColorCorner.Parent = Color
	
						ColorSelection.Name = "ColorSelection"
						ColorSelection.Parent = Color
						ColorSelection.AnchorPoint = Vector2.new(0.5, 0.5)
						ColorSelection.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
						ColorSelection.BackgroundTransparency = 1.000
						ColorSelection.Position = UDim2.new(preset and select(3, Color3.toHSV(preset)))
						ColorSelection.Size = UDim2.new(0, 18, 0, 18)
						ColorSelection.Image = "http://www.roblox.com/asset/?id=4805639000"
						ColorSelection.ScaleType = Enum.ScaleType.Fit
	
						Hue.Name = "Hue"
						Hue.Parent = ColorpickerFrame
						Hue.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
						Hue.Position = UDim2.new(0, 171, 0, 10)
						Hue.Size = UDim2.new(0, 18, 0, 118)
	
						HueCorner.CornerRadius = UDim.new(0, 3)
						HueCorner.Name = "HueCorner"
						HueCorner.Parent = Hue
	
						HueGradient.Color = ColorSequence.new {ColorSequenceKeypoint.new(0.00, Color3.fromRGB(255, 0, 4)), ColorSequenceKeypoint.new(0.20, Color3.fromRGB(234, 255, 0)), ColorSequenceKeypoint.new(0.40, Color3.fromRGB(21, 255, 0)), ColorSequenceKeypoint.new(0.60, Color3.fromRGB(0, 255, 255)), ColorSequenceKeypoint.new(0.80, Color3.fromRGB(0, 17, 255)), ColorSequenceKeypoint.new(0.90, Color3.fromRGB(255, 0, 251)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 0, 4))}
						HueGradient.Rotation = 270
						HueGradient.Name = "HueGradient"
						HueGradient.Parent = Hue
	
						HueSelection.Name = "HueSelection"
						HueSelection.Parent = Hue
						HueSelection.AnchorPoint = Vector2.new(0.5, 0.5)
						HueSelection.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
						HueSelection.BackgroundTransparency = 1.000
						HueSelection.Position = UDim2.new(0.48, 0, 1 - select(1, Color3.toHSV(preset)))
						HueSelection.Size = UDim2.new(0, 18, 0, 18)
						HueSelection.Image = "http://www.roblox.com/asset/?id=4805639000"
	
						PresetClr.Name = "PresetClr"
						PresetClr.Parent = ColorpickerFrame
						PresetClr.BackgroundColor3 = preset
						PresetClr.Position = UDim2.new(0.9, 0, 0.0740740746, 0)
						PresetClr.Size = UDim2.new(0, 20, 0, 20)
	
						PresetClrCorner.CornerRadius = UDim.new(0, 3)
						PresetClrCorner.Name = "PresetClrCorner"
						PresetClrCorner.Parent = PresetClr
	
						local function UpdateColorPicker(nope)
							PresetClr.BackgroundColor3 = Color3.fromHSV(ColorH, ColorS, ColorV)
							Color.BackgroundColor3 = Color3.fromHSV(ColorH, 1, 1)
							pcall(callback, PresetClr.BackgroundColor3)
						end
	
						ColorH = 1 - (math.clamp(HueSelection.AbsolutePosition.Y - Hue.AbsolutePosition.Y, 0, Hue.AbsoluteSize.Y) / Hue.AbsoluteSize.Y)
						ColorS = (math.clamp(ColorSelection.AbsolutePosition.X - Color.AbsolutePosition.X, 0, Color.AbsoluteSize.X) / Color.AbsoluteSize.X)
						ColorV = 1 - (math.clamp(ColorSelection.AbsolutePosition.Y - Color.AbsolutePosition.Y, 0, Color.AbsoluteSize.Y) / Color.AbsoluteSize.Y)
	
						PresetClr.BackgroundColor3 = preset
						Color.BackgroundColor3 = preset
						pcall(callback, PresetClr.BackgroundColor3)
	
						Color.InputBegan:Connect(function(input)
							if input.UserInputType == Enum.UserInputType.MouseButton1 then
								if ColorInput then
									ColorInput:Disconnect()
								end
	
								ColorInput = RunService.RenderStepped:Connect(function()
									local ColorX = (math.clamp(Mouse.X - Color.AbsolutePosition.X, 0, Color.AbsoluteSize.X) / Color.AbsoluteSize.X)
									local ColorY = (math.clamp(Mouse.Y - Color.AbsolutePosition.Y, 0, Color.AbsoluteSize.Y) / Color.AbsoluteSize.Y)
									ColorSelection.Position = UDim2.new(ColorX, 0, ColorY, 0)
									ColorS = ColorX
									ColorV = 1 - ColorY
	
									UpdateColorPicker(true)
								end)
							end
						end)
	
						Color.InputEnded:Connect(function(input)
							if input.UserInputType == Enum.UserInputType.MouseButton1 then
								if ColorInput then
									ColorInput:Disconnect()
								end
							end
						end)
	
						Hue.InputBegan:Connect(function(input)
							if input.UserInputType == Enum.UserInputType.MouseButton1 then
								if HueInput then
									HueInput:Disconnect()
								end
	
								HueInput = RunService.RenderStepped:Connect(function()
									local HueY = (math.clamp(Mouse.Y - Hue.AbsolutePosition.Y, 0, Hue.AbsoluteSize.Y) / Hue.AbsoluteSize.Y)
									HueSelection.Position = UDim2.new(0.48, 0, HueY, 0)
									ColorH = 1 - HueY
	
									UpdateColorPicker(true)
								end)
							end
						end)
	
						Hue.InputEnded:Connect(function(input)
							if input.UserInputType == Enum.UserInputType.MouseButton1 then
								if HueInput then
									HueInput:Disconnect()
								end
							end
						end)
					end

					function functionitem:AddTextbox(options)
						local Name = options.Name
						local Placeholder = options.Value
						local callback = options.Callback
	
						local Textbox = Instance.new("Frame")
						local UICorner_16 = Instance.new("UICorner")
						local Text_5 = Instance.new("TextLabel")
						local TextboxHoler = Instance.new("Frame")
						local UICorner_17 = Instance.new("UICorner")
						local HeadTitle = Instance.new("TextBox")
	
						Textbox.Name = Name
						Textbox.Parent = SectionContainer
						Textbox.BackgroundColor3 = Color3.fromRGB(1, 2, 3)
						Textbox.BackgroundTransparency = 0.700
						Textbox.BorderSizePixel = 0
						Textbox.ClipsDescendants = true
						Textbox.Size = UDim2.new(1, 0, 0, 60)
						Textbox.ZIndex = 16
						--InputEnded
						local UIStroke96 = Instance.new("UIStroke")
						UIStroke96.Thickness = 1.2
						UIStroke96.Parent = Textbox
						UIStroke96.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
						UIStroke96.LineJoinMode = Enum.LineJoinMode.Round
						UIStroke96.Color = _G.Color
						UIStroke96.Transparency = 1
	
						Textbox.MouseEnter:Connect(function()
							TweenService:Create(
								UIStroke96,
								TweenInfo.new(0.4,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
								{Transparency = 0.10}
							):Play()
						end)
	
						Textbox.MouseLeave:Connect(function()
							TweenService:Create(
								UIStroke96,
								TweenInfo.new(0.4,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
								{Transparency = 1}
							):Play()
						end)
	
						UICorner_16.CornerRadius = UDim.new(0, 4)
						UICorner_16.Parent = Textbox
	
						Text_5.Name = "Text"
						Text_5.Parent = Textbox
						Text_5.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
						Text_5.BackgroundTransparency = 1.000
						Text_5.Position = UDim2.new(0, 10, 0, 10)
						Text_5.Size = UDim2.new(0, 43, 0, 12)
						Text_5.ZIndex = 16
						Text_5.Font = Enum.Font.GothamBold
						Text_5.Text = Name
						Text_5.TextColor3 = _G.Color
						Text_5.TextSize = 11.000
						Text_5.TextXAlignment = Enum.TextXAlignment.Left
	
						TextboxHoler.Name = "TextboxHoler"
						TextboxHoler.Parent = Textbox
						TextboxHoler.AnchorPoint = Vector2.new(0.5, 0.5)
						TextboxHoler.BackgroundColor3 = Color3.fromRGB(13, 13, 15)
						TextboxHoler.BackgroundTransparency = 1.000
						TextboxHoler.BorderSizePixel = 0
						TextboxHoler.Position = UDim2.new(0.5, 0, 0.5, 13)
						TextboxHoler.Size = UDim2.new(0.970000029, 0, 0, 30)
	
						UICorner_17.CornerRadius = UDim.new(0, 8)
						UICorner_17.Parent = TextboxHoler
	
						HeadTitle.Name = "HeadTitle"
						HeadTitle.Parent = TextboxHoler
						HeadTitle.AnchorPoint = Vector2.new(0.5, 0.5)
						HeadTitle.BackgroundColor3 = Color3.fromRGB(22, 22, 22)
						HeadTitle.BackgroundTransparency = 1.000
						HeadTitle.BorderSizePixel = 0
						HeadTitle.ClipsDescendants = true
						HeadTitle.Position = UDim2.new(0.5, 3, 0.5, 0)
						HeadTitle.Size = UDim2.new(0.949999988, 0, 0, 25)
						HeadTitle.ZIndex = 16
						HeadTitle.Font = Enum.Font.GothamBold
						HeadTitle.PlaceholderColor3 = Color3.fromRGB(255, 255, 255)
						HeadTitle.PlaceholderText = Placeholder
						HeadTitle.Text = ""
						HeadTitle.TextColor3 = Color3.fromRGB(255, 255, 255)
						HeadTitle.TextSize = 13.000
						HeadTitle.TextXAlignment = Enum.TextXAlignment.Center
	
						local ButtonColor44 = Instance.new("UIStroke")
	
						ButtonColor44.Thickness = 0.9
						ButtonColor44.Name = ""
						ButtonColor44.Parent = HeadTitle
						ButtonColor44.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
						ButtonColor44.LineJoinMode = Enum.LineJoinMode.Round
						ButtonColor44.Color = _G.Color
						ButtonColor44.Transparency = 0.2
	
						Textbox.MouseEnter:Connect(function()
							TweenService:Create(
								ButtonColor44,
								TweenInfo.new(0.4,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
								{Thickness = 1}
							):Play()
							TweenService:Create(
								ButtonColor44,
								TweenInfo.new(0.4,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
								{Transparency = 0.5}
							):Play()
						end)
	
						Textbox.MouseLeave:Connect(function()
							TweenService:Create(
								ButtonColor44,
								TweenInfo.new(0.4,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
								{Thickness = 0.9}
							):Play()
							TweenService:Create(
								ButtonColor44,
								TweenInfo.new(0.4,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
								{Transparency = 0.2}
							):Play()
						end)
	
						HeadTitle.FocusLost:Connect(function(ep)
							if ep then
								if #HeadTitle.Text > 0 then
									callback(HeadTitle.Text)
									HeadTitle.Text = HeadTitle.Text
								end
							end
						end)
					end

					return functionitem
				end
				return sections
			end
		end
	end
	return tabs
end
return library
