local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local Window = OrionLib:MakeWindow({Name = "skibi toilet defense", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"})


local Tab = Window:MakeTab({
	Name = "skibi toilet defense",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})
local Section = Tab:AddSection({
	Name = "probably first script ever"
})
Tab:AddButton({
	Name = "ANTI AFK",
	Callback = function()
      		print("button pressed")
      		print("Enabled ANTI afk!")
      		local vu = game:GetService("VirtualUser")
game:GetService("Players").LocalPlayer.Idled:connect(function()
   vu:Button2Down(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
   wait(1)
   vu:Button2Up(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
end)
  	end    
})
Tab:AddButton({
	Name = "AutoSkip",
	Callback = function()
      		print("button pressed")
      		print("AutoSkip")
      		local vu = game:GetService("VirtualUser")
game:GetService("ReplicatedStorage"):WaitForChild("Resource"):WaitForChild("Remote"):WaitForChild("SkipVote"):FireServer()
while true do
game:GetService("ReplicatedStorage"):WaitForChild("Resource"):WaitForChild("Remote"):WaitForChild("SkipVote"):FireServer()
wait(0.00001)
end
  	end    
})
