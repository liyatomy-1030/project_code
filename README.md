# project_code
import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Input } from "@/components/ui/input";
import { Button } from "@/components/ui/button";

export default function InternDashboard() {
  const internName = "John Doe";
  const referralCode = "johndoe2025";
  const totalDonations = 12000;

  return (
    <div className="min-h-screen bg-gray-100 flex flex-col items-center p-6 space-y-6">
      <div className="bg-white rounded-2xl shadow-md p-6 w-full max-w-md">
        <h1 className="text-2xl font-bold text-center mb-4">Intern Portal</h1>

        {/* Dummy Login/Signup */}
        <div className="space-y-3">
          <Input placeholder="Username" />
          <Input placeholder="Password" type="password" />
          <Button className="w-full">Login</Button>
        </div>
      </div>

      <Card className="w-full max-w-md">
        <CardContent className="space-y-4 p-6">
          <h2 className="text-xl font-semibold text-center">Dashboard</h2>

          <div className="text-gray-700">Intern Name: <strong>{internName}</strong></div>
          <div className="text-gray-700">Referral Code: <strong>{referralCode}</strong></div>
          <div className="text-gray-700">Total Donations Raised: <strong>₹{totalDonations}</strong></div>

          <div className="mt-4">
            <h3 className="font-medium">Rewards / Unlockables</h3>
            <ul className="list-disc list-inside text-sm text-gray-600">
              <li>Badge: Bronze Donor</li>
              <li>Next Unlock: Silver Badge at ₹20,000</li>
              <li>Free Workshop Access at ₹50,000</li>
            </ul>
          </div>
        </CardContent>
      </Card>
    </div>
  );
}
