---
title: XRInputSourceEvent.inputSource
slug: Web/API/XRInputSourceEvent/inputSource
tags:
- API
- AR
- Controller
- Input
- Mixed
- Property
- Read-only
- Reality
- Reference
- VR
- Virtual
- WebXR
- WebXR API
- WebXR Device API
- XR
- XRInputSourceEvent
- augmented
- inputSource
- source
browser-compat: api.XRInputSourceEvent.inputSource
---
<p>{{APIRef("WebXR Device API")}}</p>

<p>The {{domxref("XRInputSourceEvent")}} interface's read-only
    <code><strong>inputSource</strong></code> property specifies the
    {{domxref("XRInputSource")}} which generated the input event. This information
  lets you handle the event appropriately given the particulars of the user input device
  being manipulated.</p>

<h2 id="Syntax">Syntax</h2>

<pre
  class="brush: js">let <em>inputSource</em> = <em>xrInputSourceEvent</em>.inputSource;</pre>

<h3 id="Value">Value</h3>

<p>An {{domxref("XRInputSource")}} object identifying the source of the user input event.
  This event indicates an action the user has taken using a WebXR input controller, such
  as a hand controller, motion sensing device, or other input apparatus.</p>

<h2 id="Example">Example</h2>

<p>The snippet below shows a handler for the {{domxref("XRSession.select_event",
  "select")}} event which looks specifically for events which happen on <code>gaze</code>
  input devices. The device type is identified by looking at the
  {{domxref("XRInputSource")}} in <code>inputSource</code> and its
  {{domxref("XRInputSource.targetRayMode", "targetRayMode")}} property.</p>

<pre class="brush: js">xrSession.onselect = event =&gt; {
  let source = event.inputSource;

  if (source.targetRayMode == "gaze") {
    /* handle selection using a gaze input */
  }
};
</pre>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

<div>{{Compat}}</div>