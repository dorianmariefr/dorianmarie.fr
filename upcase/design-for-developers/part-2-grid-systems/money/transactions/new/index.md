---
layout: money
title: New transaction
---

<h2>New transaction</h2>

<form action="../../">
  <div class="pb-4">
    <label>
      Amount
      <div class="flex items-center gap-2">
        <input type="number" step="0.01" class="!w-40" />
        €
      </div>
    </label>
  </div>

  <div class="pb-4">
    <label>
      From
      <select>
        <option>Main (425,23€)</option>
        <option>Savings (4 215,58 €)</option>
        <option>Summer 2022 (2 000,00 €)</option>
        <option>Tesla Model 3 (10 000,00 €)</option>
      </select>
    </label>
  </div>

  <div class="pb-4">
    <label>
      To
      <select></select>
    </label>
  </div>

  <div class="pb-4">
    <label>
      Description
      <input type="text" />
    </label>
  </div>

  <div class="pb-4">
    <input class="button--primary" type="submit" value="Create transaction" />
  </div>
</form>
