_G.ping = false
local mt = getrawmetatable(game);
setreadonly(mt,false)
local namecall = mt.__namecall

mt.__namecall = newcclosure(function(self, ...)
	local Method = getnamecallmethod()
	local Args = {...}

	if Method == 'FireServer' and _G.ping == false then
local test = self.Name:split("Eventv")
warn(test[2])
_G.ping = test[2]
	end
	return namecall(self, ...) 
end)
if _G.grav == nil then
    _G.grav = workspace.Gravity 
    _G.Speed = game.Players.LocalPlayer.Character.Humanoid.WalkSpeed
    _G.jump = game.Players.LocalPlayer.Character.Humanoid.JumpPower
    end
local library = loadstring(game:HttpGet("https://pastebin.com/raw/PpMcEF8z", true))()
local example = library:CreateWindow({
  text = "The Money Collector"
})
example:AddLabel("Super Code Redeemer",function()
end)
example:AddBox("Enter Code", function(object, focus)
  if focus then
 
      local code = tostring(object.Text)
      for i=1,3000 do
          task.spawn(function()
game:GetService("ReplicatedStorage").FrameworkReplicated.DataStreams["RedeemCode_Functionv".._G.ping]:InvokeServer(code)
          end)
          end
  end
end)
example:AddLabel("Super Present Claimer",function()
end)
example:AddBox("Enter Present Number", function(object, focus)
  if focus then
      local code = tonumber(object.Text)
      for i=1,1000 do
    task.spawn(function()
game:GetService("ReplicatedStorage").FrameworkReplicated.DataStreams["ClaimReward_Functionv".._G.ping]:InvokeServer(code)
end)
end
end
end)
example:AddToggle("Money AutoFarm", function(state)
_G.ok = (state and true or false)
while _G.ok do
    for o,c in pairs(workspace:GetDescendants()) do
    if c.ClassName == "Folder" and c:FindFirstChild("ResetPoint") then
for i=1,1000 do
task.spawn(function()
for i,v in pairs(c.Map.ATMs:GetChildren()) do
    if v.Name == "Model" and not v.PrimaryPart:FindFirstChild("GameTaskTimer") then
game:GetService("ReplicatedStorage").FrameworkReplicated.DataStreams["GameTaskCompleted_Functionv".._G.ping]:InvokeServer(v)
        end
        end
end)
end
end
end
wait(3)
end
end)
local example = library:CreateWindow({
  text = "Pets"
})
example:AddLabel("Delete Pets By Rarity",function()
end)
example:AddBox("Enter Pet Rarity", function(object, focus)
  if focus then
 
      local code = tostring(object.Text)
for i,v in pairs(game:GetService("Players").LocalPlayer.PlayerGui.Pets.Container.Contents.Pets:GetChildren()) do
    if v.ClassName == "TextButton" and v.Container.Description.Text == code then
game:GetService("ReplicatedStorage").FrameworkReplicated.DataStreams["ServerSellPet_Eventv".._G.ping]:FireServer(tostring(v.Name))
end
end

  end
  end)
local example = library:CreateWindow({
  text = "Misc"
})
example:AddLabel("Player Speed Changer",function()
end)
example:AddBox("Enter Speed Value", function(object, focus)
  if focus then
 
      _G.mood = tostring(object.Text)
  end
end)
example:AddToggle("Speed Enabler", function(state)
_G.speedster = (state and true or false)
while _G.speedster do
    task.wait()
    pcall(function()
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = _G.mood
    end)
    end
end)
example:AddToggle("Infinite Jump", function(state)
_G.infjump = (state and true or false)
while _G.infjump do
    task.wait()
if game.Players.LocalPlayer.Character.Humanoid.Jump == true then
game.Players.LocalPlayer.Character.Humanoid:ChangeState(3)
end
end
end)
example:AddLabel("Gravity Changer",function()
end)
example:AddBox("Enter Gravity Value", function(object, focus)
  if focus then
 
      code = tonumber(object.Text)
      workspace.Gravity = code
  end
end)      
example:AddButton("reset gravity", function(state)
workspace.Gravity = _G.grav
end)
      
local example = library:CreateWindow({
  text = "Created By"
})
example:AddLabel("MARCO POLO#3842",function()
end)
