---
- dashboard: henry_lookup_dashboard
  title: Henry Lookup Dashboard
  layout: newspaper
  description: ''
  preferred_slug: GDU8lm3fywXoRFfAFjjr85
  elements:
  - title: Field Lookup
    name: Field Lookup
    model: system__activity
    explore: field_usage
    type: looker_grid
    fields: [field_usage.model, field_usage.explore, field_usage.view, field_usage.field,
      field_usage.times_used]
    sorts: [field_usage.times_used desc 0]
    limit: 500
    column_limit: 50
    query_timezone: America/Los_Angeles
    show_view_names: false
    show_row_numbers: true
    transpose: false
    truncate_text: true
    hide_totals: false
    hide_row_totals: false
    size_to_fit: true
    table_theme: white
    limit_displayed_rows: false
    enable_conditional_formatting: false
    header_text_alignment: left
    header_font_size: 12
    rows_font_size: 12
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    defaults_version: 1
    listen:
      Field Name: field_usage.field
      Explore Name: field_usage.explore
      Model Name: field_usage.model
    row: 0
    col: 0
    width: 24
    height: 6
  - title: Historical Usage
    name: Historical Usage
    model: system__activity
    explore: history
    type: looker_grid
    fields: [history.created_time, history.id, history.source, query.formatted_fields,
      user.id, user.name, user.email]
    sorts: [history.created_time desc]
    limit: 500
    column_limit: 50
    query_timezone: America/Los_Angeles
    show_view_names: false
    show_row_numbers: true
    transpose: false
    truncate_text: true
    hide_totals: false
    hide_row_totals: false
    size_to_fit: true
    table_theme: white
    limit_displayed_rows: false
    enable_conditional_formatting: false
    header_text_alignment: left
    header_font_size: 12
    rows_font_size: 12
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    hidden_pivots: {}
    defaults_version: 1
    listen:
      Field Name: query.formatted_fields
      Explore Name: query.view
      Model Name: query.model
    row: 6
    col: 0
    width: 24
    height: 6
  - title: Dashboard Lookup
    name: Dashboard Lookup
    model: system__activity
    explore: dashboard
    type: looker_grid
    fields: [dashboard.id, dashboard.title, dashboard.link, folders.id, folders.name,
      dashboard_element.id, dashboard_element.title, query.formatted_fields]
    filters:
      dashboard.moved_to_trash: 'No'
    sorts: [dashboard.id]
    limit: 500
    column_limit: 50
    query_timezone: America/Los_Angeles
    show_view_names: false
    show_row_numbers: true
    transpose: false
    truncate_text: true
    hide_totals: false
    hide_row_totals: false
    size_to_fit: true
    table_theme: white
    limit_displayed_rows: false
    enable_conditional_formatting: false
    header_text_alignment: left
    header_font_size: 12
    rows_font_size: 12
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    defaults_version: 1
    listen:
      Field Name: query.formatted_fields
      Explore Name: query.view
      Model Name: query.model
    row: 12
    col: 0
    width: 24
    height: 6
  - title: Look Lookup
    name: Look Lookup
    model: system__activity
    explore: look
    type: looker_grid
    fields: [look.id, look.title, look.link, folders.id, folders.name, query.formatted_fields]
    sorts: [look.id]
    limit: 500
    column_limit: 50
    query_timezone: America/Los_Angeles
    show_view_names: false
    show_row_numbers: true
    transpose: false
    truncate_text: true
    hide_totals: false
    hide_row_totals: false
    size_to_fit: true
    table_theme: white
    limit_displayed_rows: false
    enable_conditional_formatting: false
    header_text_alignment: left
    header_font_size: 12
    rows_font_size: 12
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    defaults_version: 1
    listen:
      Field Name: query.formatted_fields
      Explore Name: query.view
      Model Name: query.model
    row: 18
    col: 0
    width: 24
    height: 6
  filters:
  - name: Field Name
    title: Field Name
    type: field_filter
    default_value: ''
    allow_multiple_values: true
    required: false
    ui_config:
      type: advanced
      display: popover
    model: system__activity
    explore: field_usage
    listens_to_filters: []
    field: field_usage.field
  - name: Explore Name
    title: Explore Name
    type: field_filter
    default_value: ''
    allow_multiple_values: true
    required: false
    ui_config:
      type: advanced
      display: popover
    model: system__activity
    explore: field_usage
    listens_to_filters: []
    field: field_usage.explore
  - name: Model Name
    title: Model Name
    type: field_filter
    default_value: ''
    allow_multiple_values: true
    required: false
    ui_config:
      type: advanced
      display: popover
    model: system__activity
    explore: field_usage
    listens_to_filters: []
    field: field_usage.model
