--// UI Library \\--
local File = writefile and readfile or false
local Library = false
Success, Library = pcall(function()
    return readfile("uwuware UI.lua")
end)
if Success == false then
    Library = game:HttpGet('https://raw.githubusercontent.com/Just-Egg-Salad/roblox-scripts/main/uwuware')
    if File then
        writefile("uwuware UI.lua", Library)
    end
end
Library = loadstring(Library)()
local Window = Library:CreateWindow("made by puro#4730")

Window:AddToggle({
    text = "autofarm",
    callback = function()
while task.wait(0) and Library.flags.autofarm do
wait(0)
local args = {
    [1] = "Phone"
}

game:GetService("ReplicatedStorage").Events.SendTexts:FireServer(unpack(args))
wait(0)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-223.693, 8.5058, 896.279)
wait(0)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-229.071, 8.63418, 912.173)

        end
	end
})


Window:AddToggle({
    text = "autocharge",
    callback = function()
while task.wait(0) and Library.flags.autocharge do
local args = {
    [1] = "Phone"
}

game:GetService("ReplicatedStorage").Events.SendTexts:FireServer(unpack(args))

local args = {
    [1] = true,
    [2] = "ChargerConnector4"
}

game:GetService("ReplicatedStorage").Events.ChargeC:FireServer(unpack(args))

        end
	end
})


Window:AddToggle({
    text = "DUPE",
    callback = function()
while task.wait(0) and Library.flags.DUPE do
local args = {
    [1] = 2
}

game:GetService("ReplicatedStorage").Events.HackingTermStart:FireServer(unpack(args))

local args = {
    [1] = workspace.HackingTerminals.Hack2.HackColor.Wedge.Rewards
}

game:GetService("ReplicatedStorage").Events.TerminalReward:FireServer(unpack(args))

game:GetService("ReplicatedStorage").MGNShared.GetPortalModelsFolder:InvokeServer()


        end
	end
})

Library:Init()
