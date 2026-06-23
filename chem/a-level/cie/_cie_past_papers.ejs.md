```{=html}
<table class="quarto-listing-table table table-hover">
  <thead>
    <tr>
      <th class="sort" data-sort="listing-year">Year</th>
      <th class="sort" data-sort="listing-season">Session</th>
      <th class="sort" data-sort="listing-paper">Paper</th>
      <th class="sort" data-sort="listing-variant">Variant</th>
      <th>QP</th>
      <th>MS</th>
    </tr>
  </thead>
  <tbody class="list">
    <% for (const item of items) { %>
      <tr <%= metadataAttrs(item) %>>
        <td class="listing-year"><%= item.year %></td>
        <td class="listing-season"><%= item.season %></td>
        <td class="listing-paper"><%= item.paper %></td>
        <td class="listing-variant"><%= item.variant %></td>
        <td class="listing-qp">
          <% if (item.qp) { %>
            <a href="<%- item.qp %>" class="btn btn-sm btn-primary bi bi-file-earmark-text" target="_blank" title="Download Question Paper" style="padding: 0.35rem 0.5rem; font-size: 0.9rem; text-decoration: none; display: inline-flex; align-items: center; justify-content: center; border-radius: 6px; width: 32px; height: 32px;"></a>
          <% } else { %>
            <span class="text-muted" style="font-size: 0.85rem;">N/A</span>
          <% } %>
        </td>
        <td class="listing-ms">
          <% if (item.ms) { %>
            <a href="<%- item.ms %>" class="btn btn-sm btn-success bi bi-key" target="_blank" title="Download Mark Scheme" style="padding: 0.35rem 0.5rem; font-size: 0.9rem; text-decoration: none; display: inline-flex; align-items: center; justify-content: center; border-radius: 6px; width: 32px; height: 32px;"></a>
          <% } else { %>
            <span class="text-muted" style="font-size: 0.85rem;">N/A</span>
          <% } %>
        </td>
      </tr>
    <% } %>
  </tbody>
</table>
```
