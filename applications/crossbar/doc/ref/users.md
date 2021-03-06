### Users

#### About Users

#### Schema

Schema for a user

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`call_forward` | The device call forward parameters | `object` |   | `false`
`call_forward.direct_calls_only` | Determines if the calls that are not directly sent to the device should be forwarded | `boolean` | `false` | `false`
`call_forward.enabled` | Determines if the call forwarding should be used | `boolean` | `false` | `false`
`call_forward.failover` | Enable the call-forwarding parameters if the device is offline | `boolean` | `false` | `false`
`call_forward.ignore_early_media` | The option to determine if early media from the call forwarded number should ignored | `boolean` | `true` | `false`
`call_forward.keep_caller_id` | Determines if the caller id is kept when the call is forwarded, if not the devices caller id is used | `boolean` | `true` | `false`
`call_forward.number` | The number to forward calls to | `string(0..35)` |   | `false`
`call_forward.require_keypress` | Determines if the callee is prompted to press 1 to accept the call | `boolean` | `true` | `false`
`call_forward.substitute` | Determines if the call forwarding replaces the device | `boolean` | `true` | `false`
`call_restriction` | Device level call restrictions for each available number classification | `object` | `{}` | `false`
`call_waiting` |   | [#/definitions/call_waiting](#call_waiting) |   | `false`
`caller_id` | The device caller ID parameters | `object` | `{}` | `false`
`contact_list` | Contect List Parameters | `object` | `{}` | `false`
`contact_list.exclude` | If set to true the device is excluded from the contact list | `boolean` |   | `false`
`dial_plan` | A list of rules used to modify dialed numbers | `object` | `{}` | `false`
`directories` | Provides the mappings for what directory the user is a part of (the key), and what callflow (the value) to invoke if the user is selected by the caller. | `object` |   | `false`
`do_not_disturb` | DND Parameters | `object` |   | `false`
`do_not_disturb.enabled` | Is do-not-disturb enabled for this user? | `boolean` |   | `false`
`email` | The email of the user | `string(1..254)` |   | `false`
`enabled` | Determines if the user is currently enabled | `boolean` | `true` | `false`
`feature_level` | The user level for assigning feature sets | `string` |   | `false`
`first_name` | The first name of the user | `string(1..128)` |   | `true`
`hotdesk` | The user hotdesk parameters | `object` | `{}` | `false`
`hotdesk.enabled` | Determines if the user has hotdesking enabled | `boolean` | `false` | `false`
`hotdesk.id` | The users hotdesk id | `string(0..15)` |   | `false`
`hotdesk.keep_logged_in_elsewhere` | Determines if user should be able to login to mutliple phones simultaneously | `boolean` | `false` | `false`
`hotdesk.pin` | The users hotdesk pin number | `string(4..15)` |   | `false`
`hotdesk.require_pin` | Determines if user requires a pin to change the hotdesk state | `boolean` | `false` | `false`
`language` | The language for this user | `string` |   | `false`
`last_name` | The last name of the user | `string(1..128)` |   | `true`
`media` | The device media parameters | `object` | `{}` | `false`
`media.audio` | The audio media parameters | `object` | `{}` | `false`
`media.audio.codecs` | A list of audio codecs the device supports | `array(string('OPUS', 'CELT@32000h', 'G7221@32000h', 'G7221@16000h', 'G722', 'speex@32000h', 'speex@16000h', 'PCMU', 'PCMA', 'G729', 'GSM', 'CELT@48000h', 'CELT@64000h', 'G722_16', 'G722_32', 'CELT_48', 'CELT_64', 'Speex', 'speex'))` | `["PCMU"]` | `false`
`media.audio.codecs.[]` |   | `string` |   | `false`
`media.bypass_media` | Default bypass media mode | `boolean, string('true', 'false', 'auto')` |   | `false`
`media.encryption` | Encryption Parameters | `object` | `{}` | `false`
`media.encryption.enforce_security` | Is Encryption Enabled? | `boolean` | `false` | `false`
`media.encryption.methods` | Supported Encryption Types | `array(string('zrtp', 'srtp'))` | `[]` | `false`
`media.encryption.methods.[]` |   | `string` |   | `false`
`media.fax_option` | Is T.38 Supported? | `boolean` |   | `false`
`media.ignore_early_media` | The option to determine if early media from the device should always be ignored | `boolean` |   | `false`
`media.progress_timeout` | The progress timeout to apply to the device (seconds) | `integer` |   | `false`
`media.video` | The video media parameters | `object` | `{}` | `false`
`media.video.codecs` | A list of video codecs the device supports | `array(string('H261', 'H263', 'H264', 'VP8'))` | `[]` | `false`
`media.video.codecs.[]` |   | `string` |   | `false`
`metaflows` | The device metaflow parameters | [#/definitions/metaflows](#metaflows) |   | `false`
`music_on_hold` | The music on hold parameters used if not a property of the device owner | `object` | `{}` | `false`
`music_on_hold.media_id` | The ID of a media object that should be used as the music on hold | `string(0..128)` |   | `false`
`password` | The GUI login password | `string` |   | `false`
`presence_id` | Static presence ID (used instead of SIP username) | `string` |   | `false`
`priv_level` | The privilege level of the user | `string('user', 'admin')` | `user` | `false`
`profile` | User's profile data | `object` | `{}` | `false`
`pronounced_name` | Name pronounced by user to introduce himself to conference members | `object` |   | `false`
`pronounced_name.media_id` | The ID of a media object that should be used as the music on hold | `string(0..128)` |   | `false`
`require_password_update` | UI flag that the user should update their password. | `boolean` | `false` | `false`
`ringtones` | Ringtone Parameters | `object` | `{}` | `false`
`ringtones.external` | The alert info SIP header added when the call is from internal sources | `string(0..256)` |   | `false`
`ringtones.internal` | The alert info SIP header added when the call is from external sources | `string(0..256)` |   | `false`
`timezone` | User's timezone | `string` |   | `false`
`username` | The GUI login username - alpha-numeric, dashes, at symbol, periods, plusses, and underscores allowed | `string(1..256)` |   | `false`
`verified` | Determines if the user has been verified | `boolean` | `false` | `false`
`vm_to_email_enabled` | Determines if the user would like voicemails emailed to them | `boolean` | `true` | `false`
`voicemail` |   | `object` |   | `false`
`voicemail.notify` |   | `object` |   | `false`
`voicemail.notify.callback` |   | [#/definitions/notify.callback](#notifycallback) |   | `false`


##### call_waiting

Parameters for server-side call waiting

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`enabled` | Determines if server side call waiting is enabled/disabled | `boolean` |   | `false`

##### caller_id

Defines caller ID settings based on the type of call being made

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`emergency` | The caller ID used when a resource is flagged as 'emergency' | `object` |   | `false`
`emergency.name` | The caller id name for the object type | `string(0..35)` |   | `false`
`emergency.number` | The caller id name for the object type | `string(0..35)` |   | `false`
`external` | The default caller ID used when dialing external numbers | `object` |   | `false`
`external.name` | The caller id name for the object type | `string(0..35)` |   | `false`
`external.number` | The caller id name for the object type | `string(0..35)` |   | `false`
`internal` | The default caller ID used when dialing internal extensions | `object` |   | `false`
`internal.name` | The caller id name for the object type | `string(0..35)` |   | `false`
`internal.number` | The caller id name for the object type | `string(0..35)` |   | `false`

##### dialplans

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`system` | List of system dial plans | `array()` |   | `false`

##### metaflow

A metaflow node defines a module to execute, data to provide to that module, and one or more children to branch to

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------

##### metaflow.audio_level

audio_level metaflow schema

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`children` |   | [#/definitions/metaflow_children](#metaflow_children) |   | `false`
`data` |   | `object` |   | `true`
`data.action` |   | `string` |   | `true`
`data.level` |   | `string` |   | `false`
`data.mode` |   | `string` |   | `false`
`module` |   | `string('audio_level')` |   | `true`

##### metaflow.break

break metaflow schema

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`children` |   | [#/definitions/metaflow_children](#metaflow_children) |   | `false`
`data` |   | `object` |   | `false`
`module` |   | `string('break')` |   | `true`

##### metaflow.callflow

callflow metaflow schema

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`children` |   | [#/definitions/metaflow_children](#metaflow_children) |   | `false`
`data` |   | `object` |   | `true`
`data.id` |   | `string` |   | `true`
`module` |   | `string('callflow')` |   | `true`

##### metaflow.hangup

hangup metaflow schema

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`children` |   | [#/definitions/metaflow_children](#metaflow_children) |   | `false`
`data` |   | `object` |   | `false`
`module` |   | `string('hangup')` |   | `true`

##### metaflow.hold

hold metaflow schema

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`children` |   | [#/definitions/metaflow_children](#metaflow_children) |   | `false`
`data` |   | `object` |   | `true`
`data.moh_aleg` |   | `string` |   | `false`
`data.moh_bleg` |   | `string` |   | `false`
`data.unhold_key` |   | `string` | `1` | `false`
`module` |   | `string('hold')` |   | `true`

##### metaflow.hold_control

hold_control metaflow schema

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`children` |   | [#/definitions/metaflow_children](#metaflow_children) |   | `false`
`data` |   | `object` |   | `false`
`data.action` |   | `string('hold', 'unhold', 'toggle')` | `toggle` | `false`
`module` |   | `string('hold_control')` |   | `true`

##### metaflow.intercept

intercept metaflow schema

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`children` |   | [#/definitions/metaflow_children](#metaflow_children) |   | `false`
`data` |   | `object` |   | `true`
`data.auto_answer` |   | `boolean` | `false` | `false`
`data.target_id` |   | `string` |   | `true`
`data.target_type` |   | `string('device', 'user', 'number')` |   | `true`
`data.unbridged_only` |   | `boolean` | `true` | `false`
`module` |   | `string('intercept')` |   | `true`

##### metaflow.move

move metaflow schema

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`children` |   | [#/definitions/metaflow_children](#metaflow_children) |   | `false`
`data` |   | `object` |   | `true`
`data.auto_answer` |   | `boolean` | `false` | `false`
`data.device_id` |   | `string` |   | `false`
`data.owner_id` |   | `string` |   | `false`
`module` |   | `string('move')` |   | `true`

##### metaflow.play

play metaflow schema

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`children` |   | [#/definitions/metaflow_children](#metaflow_children) |   | `false`
`data` |   | `object` |   | `true`
`data.id` |   | `string` |   | `true`
`data.leg` |   | `string('both', 'self', 'peer')` | `both` | `false`
`module` |   | `string('play')` |   | `true`

##### metaflow.record_call

record_call metaflow schema

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`children` |   | [#/definitions/metaflow_children](#metaflow_children) |   | `false`
`data` |   | `object` |   | `true`
`data.action` |   | `string('start', 'stop', 'toggle')` | `toggle` | `true`
`data.format` |   | `string` |   | `false`
`data.media_name` |   | `string` |   | `false`
`module` |   | `string('record_call')` |   | `true`

##### metaflow.resume

resume metaflow schema

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`children` |   | [#/definitions/metaflow_children](#metaflow_children) |   | `false`
`data` |   | `object` |   | `false`
`module` |   | `string('resume')` |   | `true`

##### metaflow.say

say metaflow schema

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`children` |   | [#/definitions/metaflow_children](#metaflow_children) |   | `false`
`data` |   | `object` |   | `true`
`data.language` |   | `string` |   | `false`
`data.method` |   | `string` |   | `false`
`data.text` |   | `string` |   | `true`
`data.type` |   | `string` |   | `false`
`module` |   | `string('say')` |   | `true`

##### metaflow.sound_touch

sound_touch metaflow schema

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`children` |   | [#/definitions/metaflow_children](#metaflow_children) |   | `false`
`data` |   | `object` |   | `true`
`data.action` |   | `string('start', 'stop')` |   | `true`
`data.adjust_in_octaves` |   | `integer` |   | `false`
`data.adjust_in_semitones` |   | `integer` |   | `false`
`data.hook_dtmf` |   | `boolean` | `false` | `false`
`data.pitch` |   | `integer` |   | `false`
`data.rate` |   | `integer` |   | `false`
`data.sending_leg` |   | `boolean` | `false` | `false`
`data.tempo` |   | `integer` |   | `false`
`module` |   | `string('sound_touch')` |   | `true`

##### metaflow.transfer

transfer metaflow schema

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`children` |   | [#/definitions/metaflow_children](#metaflow_children) |   | `false`
`data` |   | `object` |   | `true`
`data.Transfer-Type` |   | `string` | `attended` | `false`
`data.captures` |   | `string` |   | `false`
`data.target` |   | `string` |   | `false`
`module` |   | `string('transfer')` |   | `true`

##### metaflow.tts

tts metaflow schema

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`children` |   | [#/definitions/metaflow_children](#metaflow_children) |   | `false`
`data` |   | `object` |   | `true`
`data.engine` |   | `string` | `flite` | `false`
`data.language` |   | `string` |   | `false`
`data.leg` |   | `string` | `self` | `false`
`data.terminators` |   | `string` |   | `false`
`data.text` |   | `string` |   | `true`
`data.voice` |   | `string` | `female` | `false`
`module` |   | `string('tts')` |   | `true`

##### metaflow_children

A metaflow child nodes

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------

##### metaflows

Actions applied to a call outside of the normal callflow, initiated by the caller(s)

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`binding_digit` | What DTMF will trigger the collection and analysis of the subsequent DTMF sequence | `string('1', '2', '3', '4', '5', '6', '7', '8', '9', '0', '*', '#')` | `*` | `false`
`digit_timeout` | How long to wait between DTMF presses before processing the collected sequence (milliseconds) | `integer` |   | `false`
`listen_on` | Which leg(s) of the call to listen for DTMF | `string('both', 'self', 'peer')` |   | `false`
`numbers` | A list of static numbers with their flows | `object` |   | `false`
`numbers./^[0-9]+$/` |   | [#/definitions/metaflow](#metaflow) |   | `false`
`patterns` | A list of patterns with their flows | `object` |   | `false`
`patterns./.+/` |   | [#/definitions/metaflow](#metaflow) |   | `false`

##### notify.callback

Schema for a callback options

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`attempts` | How many attempts without answer will system do | `integer` |   | `false`
`disabled` | Determines if the system will call to callback number | `boolean` |   | `false`
`interval_s` | How long will system wait between call back notification attempts | `integer` |   | `false`
`number` | Number for callback notifications about new messages | `string` |   | `false`
`schedule` | Schedules interval between callbacks | `array(integer)` |   | `false`
`timeout_s` | How long will system wait for answer to callback | `integer` |   | `false`

##### profile

Defines user extended properties

Key | Description | Type | Default | Required
--- | ----------- | ---- | ------- | --------
`addresses` | To specify the components of the addresses | `array(object)` |   | `false`
`addresses.[].address` | To specify the address | `string` |   | `false`
`addresses.[].types` | To specify types of the address | `array()` |   | `false`
`assistant` | To specify the user's assistant | `string` |   | `false`
`birthday` | To specify the birth date of the user | `string` |   | `false`
`nicknames` | To specify the text corresponding to the nickname of the user | `array(string)` |   | `false`
`nicknames.[]` |   | `string` |   | `false`
`note` | To specify supplemental information or a comment that is associated with the user | `string` |   | `false`
`role` | To specify the function or part played in a particular situation by the user | `string` |   | `false`
`sort-string` | To specify the family name or given name text to be used for national-language-specific sorting of the FN and N types | `string` |   | `false`
`title` | To specify the position or job of the user | `string` |   | `false`



#### Fetch

> GET /v2/accounts/{ACCOUNT_ID}/users

```shell
curl -v -X GET \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users
```

#### Create

> PUT /v2/accounts/{ACCOUNT_ID}/users

```shell
curl -v -X PUT \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users
```

#### Fetch

> GET /v2/accounts/{ACCOUNT_ID}/users/{USER_ID}

```shell
curl -v -X GET \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users/{USER_ID}
```

#### Change

> POST /v2/accounts/{ACCOUNT_ID}/users/{USER_ID}

```shell
curl -v -X POST \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users/{USER_ID}
```

#### Patch

> PATCH /v2/accounts/{ACCOUNT_ID}/users/{USER_ID}

```shell
curl -v -X PATCH \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users/{USER_ID}
```

#### Remove

> DELETE /v2/accounts/{ACCOUNT_ID}/users/{USER_ID}

```shell
curl -v -X DELETE \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users/{USER_ID}
```

#### Fetch

> GET /v2/accounts/{ACCOUNT_ID}/users/{USER_ID}/vcard

```shell
curl -v -X GET \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users/{USER_ID}/vcard
```

#### Fetch

> GET /v2/accounts/{ACCOUNT_ID}/users/{USER_ID}/photo

```shell
curl -v -X GET \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users/{USER_ID}/photo
```

#### Change

> POST /v2/accounts/{ACCOUNT_ID}/users/{USER_ID}/photo

```shell
curl -v -X POST \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users/{USER_ID}/photo
```

#### Remove

> DELETE /v2/accounts/{ACCOUNT_ID}/users/{USER_ID}/photo

```shell
curl -v -X DELETE \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users/{USER_ID}/photo
```

#### Fetch

> GET /v2/accounts/{ACCOUNT_ID}/users/{USER_ID}/quickcall/{PHONE_NUMBER}

```shell
curl -v -X GET \
    -H "X-Auth-Token: {AUTH_TOKEN}" \
    http://{SERVER}:8000/v2/accounts/{ACCOUNT_ID}/users/{USER_ID}/quickcall/{PHONE_NUMBER}
```

