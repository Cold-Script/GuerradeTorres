local repo = "https://raw.githubusercontent.com/mstudio45/LinoriaLib/main/"

local Library = loadstring(game:HttpGet(repo .. "Library.lua"))()
local ThemeManager = loadstring(game:HttpGet(repo .. "addons/ThemeManager.lua"))()
local SaveManager = loadstring(game:HttpGet(repo .. "addons/SaveManager.lua"))()
local Options = getgenv().Linoria.Options
local Toggles = getgenv().Linoria.Toggles

local Window = Library:CreateWindow({
	Title = "YPoint | Guerra de Torres",
	Center = true,
	AutoShow = true,
	Resizable = true,
	ShowCustomCursor = true,
	TabPadding = 2,
	MenuFadeTime = 
})

speed = 16

Tabs = {
Main = Window:AddTab("Main"),
Visual = Window:AddTab("Visual"),
Configs = Window:AddTab("Config")
}
Group = {
Main1 = Tabs.Main:AddTab("Players"),
}
Group.Main1:AddSlider("",{
Text = "Speed Boost",
Tooltip = "Boost Speed Players",
Default = 1,
Min = 1,
Max = 8,
Compact = 1,
Rounding = true,
Callback = function(v)
game:GetService("RunService").RenderStepped:Connect(function()
speed = v
end)
if speed = "1" then
game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 16
elseif speed = "2" then
game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 18
elseif speed = "3" then
game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 20
elseif speed = "4" then
game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 22
elseif speed = "5" then
game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 24
elseif speed = "6" then
game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 26
elseif speed = "7" then
game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 28
elseif speed = "8" then
game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 30
end})
