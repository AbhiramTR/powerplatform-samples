# Samples by Compatibility

All samples are compatible with SharePoint Online. If you wish to find web parts that were specifically designed for SharePoint 2019 or Microsoft Teams, use the filters below.

To learn more about how to use these samples, please refer to our [getting started](../gettingstarted/index.md) section.

 <div class="well">
  <div class="button-group filters-button-group">
    <button class="button is-checked" data-filter="*">All</button>
    <button class="button" data-filter="*">SharePoint Online</button>
    <button class="button" data-filter="[data-compatibility*='SharePoint 2019'],[data-spfx='1.4.1']">SharePoint
      2019</button>
    <button class="button" data-filter="[data-compatibility*='Microsoft Teams']">Microsoft Teams</button>
<button class="button" data-filter="[data-compatibility*='Outlook']">Outlook</button>
  </div>
</div>

<div class="grid">

{% for sample in samples|sort(attribute='modified', reverse=True) %}

<div class="sample-item" data-framework="{{sample.framework}}" data-spfx="{{sample.spfx}}" data-modified="{{sample.modified}}" data-title="{{ sample.title }}" data-compatibility="{{ sample.compatibility }}"  data-thumbnail="{{sample.thumbnail}}">
  <div class="sample">
    <div class="sample-video"><i class="ms-Icon ms-Icon--VideoSolid" aria-hidden="true"></i></div>
    <div class="sample-img">
      <a class="sample-link"
        href="{{sample.url}}"
        title="{{sample.summary}}">
        <picture>
          <img src="../../img/thumbnails/sm/{{ sample.name }}.png" width="302" alt="{{sample.name}}" data-fullsize="{{sample.thumbnail}}" data-orig="../../img/thumbnails/sm/{{ sample.name }}.png"/>
        </picture>
      </a>
    </div>
  </div>
      <a href="{{sample.url}}"
      title="{{ sample.summary }}">
<span class="location" title="Compatible with: {{sample.compatibility}}">{{ sample.compatibility }}</span>
  <h2 class="name">
      {{sample.title}}</h2>
      <div class="sample-activity">
  <span class="author" title="{{ sample.author }}">{{ sample.author }}</span>
  <span class="modified">Modified {{ sample.modifiedtext }}</span>
  </div>
  </a>

</div>
    {% endfor %}
</div>

<img src="https://telemetry.sharepointpnp.com/sp-dev-fx-webparts/docs/samples/compatibility" />