import React from 'react';
import Head from 'next/head';
import * as Tabs from '@radix-ui/react-tabs';
import * as Checkbox from '@radix-ui/react-checkbox';
import * as DropdownMenu from '@radix-ui/react-dropdown-menu';

const ImpoundsPage: React.FC = () => {
  return (
    <div className="bg-gray-100 min-h-screen">
      <Head>
        <title>FoxTow - Impounds</title>
      </Head>
      <header className="bg-blue-800 text-white p-4">
        <div className="flex items-center justify-between">
          <div className="flex items-center space-x-4">
            <img src="/logo.png" alt="FoxTow Logo" className="h-8" />
            <nav className="space-x-4">
              <a href="#" className="hover:underline">Dashboard</a>
              <a href="#" className="hover:underline">Dispatching</a>
              <a href="#" className="hover:underline">Map</a>
              <a href="#" className="hover:underline">Impounds</a>
              <a href="#" className="hover:underline">Accounts</a>
              <a href="#" className="hover:underline">Reports</a>
              <a href="#" className="hover:underline">Settings</a>
            </nav>
          </div>
          <div className="flex items-center space-x-4">
            <span>Certified Towing</span>
            <span>Programmeri (Manager)</span>
            <button className="bg-blue-600 px-3 py-1 rounded">S</button>
          </div>
        </div>
      </header>
      <main className="p-6">
        <div className="bg-white rounded-lg shadow p-6">
          <div className="flex justify-between mb-4">
            <div className="space-x-2">
              <button className="bg-blue-600 text-white px-4 py-2 rounded">+ New Impound</button>
              <button className="bg-blue-600 text-white px-4 py-2 rounded">Create Report</button>
            </div>
            <div>
              <select className="border rounded px-2 py-1">
                <option>Filter By: All</option>
              </select>
            </div>
          </div>
          <Tabs.Root defaultValue="current">
            <Tabs.List className="flex border-b mb-4">
              <Tabs.Trigger value="current" className="px-4 py-2 border-b-2 border-transparent hover:border-blue-500">Current (1)</Tabs.Trigger>
              <Tabs.Trigger value="released" className="px-4 py-2 border-b-2 border-transparent hover:border-blue-500">Released</Tabs.Trigger>
              <Tabs.Trigger value="auction" className="px-4 py-2 border-b-2 border-transparent hover:border-blue-500">Auction</Tabs.Trigger>
              <Tabs.Trigger value="all" className="px-4 py-2 border-b-2 border-transparent hover:border-blue-500">All</Tabs.Trigger>
            </Tabs.List>
            <Tabs.Content value="current">
              <table className="w-full">
                <thead>
                  <tr className="text-left">
                    <th><Checkbox.Root className="mr-2" /></th>
                    <th>Stock #</th>
                    <th>Call #</th>
                    <th>Invoice #</th>
                    <th>Account</th>
                    <th>Storage</th>
                    <th>Driver</th>
                    <th>Days Held</th>
                    <th>Vehicle</th>
                    <th>Plate</th>
                    <th>VIN</th>
                    <th>Impound Date</th>
                    <th>Total</th>
                    <th>Balance</th>
                    <th>Tasks</th>
                    <th>Color</th>
                    <th>Make</th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <td><Checkbox.Root className="mr-2" /></td>
                    <td>19437362</td>
                    <td>5463</td>
                    <td></td>
                    <td>Richmond Police Department</td>
                    <td>Certified Towing Lot 1</td>
                    <td>Humberto Benavidez</td>
                    <td>1</td>
                    <td>1998 GMC Yukon Red</td>
                    <td>44353M3</td>
                    <td>1GKEK13R1WJ716695</td>
                    <td>7/17/2024 9:28 AM</td>
                    <td>$250.00</td>
                    <td>$250.00</td>
                    <td>
                      <span className="bg-green-200 text-green-800 px-2 py-1 rounded text-xs">Due Next</span>
                      <span className="bg-red-200 text-red-800 px-2 py-1 rounded text-xs">Due Today</span>
                      <span className="bg-green-200 text-green-800 px-2 py-1 rounded text-xs">Due Next</span>
                    </td>
                    <td>Red</td>
                    <td>GMC</td>
                  </tr>
                </tbody>
              </table>
            </Tabs.Content>
          </Tabs.Root>
        </div>
      </main>
    </div>
  );
};

export default ImpoundsPage;
