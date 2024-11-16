# homeassistant-dashboards

<p>🧳 Welcome traveler!</p>
<p>🐈 I am Pablo your host.</p>
<p>🔥 Come in. Put your feet up by the fire.</p>
<p>🍺 Pour a glass of beer, while we learn a few tricks in homeassistant.</p>

<p></p>

# Home Assistant

<p>👑 A wise person once said 'My home is my kingdom' &nbsp;  &nbsp; or was it <i>'I fart in your general direction!'</i> <link>https://www.youtube.com/watch?v=QSo0duY7-9s&t=4s</link></p>
<p>🏡 Home Assistant - where the Holy Grail of energy monitoring meets smart home sovereignty. Control your kingdom's devices, automate your noble chores, and may your wattage be ever in your favor.
  
# Energy Monitoring

Using the Custom Bubble Card we can create the below.

<img width="520" alt="Screenshot 2024-11-16 at 11 58 04" src="https://github.com/user-attachments/assets/eab3efae-aab5-479f-a44d-24cf4979502e">


```
type: horizontal-stack
cards:
  - type: vertical-stack
    cards:
      - type: custom:bubble-card
        card_type: separator
        name: Power
        sub_button:
          - entity: sensor.smart_meter_electricity_import_this_month
            show_state: true
        styles: |-
          .bubble-sub-button-1 {
              background-color: black !important;
            }
      - type: horizontal-stack
        cards:
          - type: vertical-stack
            cards:
              - type: custom:bubble-card
                card_type: button
                button_type: state
                entity: sensor.house_net_energy_usage_now
                name: Miscellaneous
                sub_button:
                  - icon: mdi:chart-line
                    entity: sensor.house_net_energy_usage_month
                    show_state: true
                    show_icon: true
                styles: |2-

                    .bubble-icon {
                      color: rgb(10, 11, 0, ) !important;
                    }

                   
                    .bubble-sub-button-1 {
                      background-color: black !important;
                    }

                    
                    .bubble-button-card-container {
                      background: rgba(20,100,100,0.1) !important;
                    }
              - type: custom:bubble-card
                card_type: separator
              - type: custom:bubble-card
                card_type: button
                button_type: state
                entity: sensor.11_smart_plug_current_power
                name: Freezer
                sub_button:
                  - icon: mdi:chart-line
                    entity: sensor.11_smart_plug_month_energy
                    show_state: true
                    show_icon: true
                styles: |2-

                    .bubble-icon {
                      color: rgb(70, 130, 180) !important;
                    }

                   
                    .bubble-sub-button-1 {
                      background-color: black !important;
                    }

                    
                    .bubble-button-card-container {
                      background: rgba(0,90,190,0.2) !important;
                    }
              - type: custom:bubble-card
                card_type: button
                button_type: state
                entity: sensor.10_smart_plug_current_power
                name: Fridge
                sub_button:
                  - icon: mdi:chart-line
                    entity: sensor.10_smart_plug_month_energy
                    show_state: true
                    show_icon: true
                styles: |2-

                    .bubble-icon {
                      color: rgb(80, 130, 180) !important;
                    }

                   
                    .bubble-sub-button-1 {
                      background-color: black !important;
                    }

                    
                    .bubble-button-card-container {
                      background: rgba(0,90,190,0.2) !important;
                    }
                force_icon: false
                scrolling_effect: true
                show_name: true
                show_state: true
              - type: custom:bubble-card
                card_type: button
                button_type: state
                entity: sensor.8_smart_plug_current_power
                name: Hen's Fridge
                sub_button:
                  - icon: mdi:chart-line
                    entity: sensor.8_smart_plug_month_energy
                    show_state: true
                    show_icon: true
                styles: |2-

                    .bubble-icon {
                      color: rgb(70, 130, 180) !important;
                    }

                   
                    .bubble-sub-button-1 {
                      background-color: black !important;
                    }

                    
                    .bubble-button-card-container {
                      background: rgba(0,90,190,0.2) !important;
                    }
              - type: custom:bubble-card
                card_type: button
                button_type: state
                entity: sensor.3_smart_plug_current_power
                name: Ed's Fridge
                sub_button:
                  - icon: mdi:chart-line
                    entity: sensor.3_smart_plug_month_energy
                    show_state: true
                    show_icon: true
                styles: |2-

                    .bubble-icon {
                      color: rgb(70, 130, 180) !important;
                    }

                   
                    .bubble-sub-button-1 {
                      background-color: black !important;
                    }

                    
                    .bubble-button-card-container {
                      background: rgba(0,90,190,0.2) !important;
                    }
              - type: custom:bubble-card
                card_type: button
                button_type: state
                entity: sensor.14_smart_plug_current_power
                name: Internet CCTV
                sub_button:
                  - icon: mdi:chart-line
                    entity: sensor.14_smart_plug_month_energy
                    show_state: true
                    show_icon: true
                styles: |2-

                    .bubble-icon {
                      color: green !important;
                    }

                   
                    .bubble-sub-button-1 {
                      background-color: black !important;
                    }

                    
                    .bubble-button-card-container {
                      background: rgba(12,120,50,0.2) !important;
                    }
              - type: custom:bubble-card
                card_type: button
                button_type: state
                entity: sensor.1_smart_plug_current_power
                name: Unraid Server
                sub_button:
                  - icon: mdi:chart-line
                    entity: sensor.1_smart_plug_month_energy
                    show_state: true
                styles: |2-

                    .bubble-icon {
                      color: green !important;
                    }

                   
                    .bubble-sub-button-1 {
                      background-color: black !important;
                    }

                    
                    .bubble-button-card-container {
                      background: rgba(12,120,50,0.2) !important;
                    }
          - type: vertical-stack
            cards:
              - type: custom:bubble-card
                card_type: button
                button_type: state
                entity: sensor.house_energy_plugs_usage_now
                name: All Plugs
                sub_button:
                  - icon: mdi:chart-line
                    entity: sensor.house_energy_plugs_usage_month
                    show_state: true
                    show_icon: true
                styles: |2-

                    .bubble-icon {
                      color: rgb(10, 11, 0,) !important;
                    }

                   
                    .bubble-sub-button-1 {
                      background-color: black !important;
                    }

                    
                    .bubble-button-card-container {
                      background: rgba(20,100,100,0.1) !important;
                    }
              - type: custom:bubble-card
                card_type: separator
              - type: custom:bubble-card
                card_type: button
                button_type: state
                entity: sensor.7_smart_plug_current_power
                name: Kettle
                sub_button:
                  - icon: mdi:chart-line
                    entity: sensor.7_smart_plug_month_energy
                    show_state: true
                    show_icon: true
                styles: |2-

                    .bubble-icon {
                      color: rgb(220, 20, 60) !important;
                    }

                   
                    .bubble-sub-button-1 {
                      background-color: black !important;
                    }

                    
                    .bubble-button-card-container {
                      background: rgba(120,10,10,0.2) !important;
                    }
              - type: custom:bubble-card
                card_type: button
                button_type: state
                entity: sensor.4_smart_plug_current_power
                name: Air Fryer
                sub_button:
                  - icon: mdi:chart-line
                    entity: sensor.4_smart_plug_month_energy
                    show_state: true
                    show_icon: true
                styles: |2-

                    .bubble-icon {
                      color: rgb(220, 20, 60) !important;
                    }

                   
                    .bubble-sub-button-1 {
                      background-color: black !important;
                    }

                    
                    .bubble-button-card-container {
                      background: rgba(120,10,10,0.2) !important;
                    }
              - type: custom:bubble-card
                card_type: button
                button_type: state
                entity: sensor.smart_plug_19_current_power
                name: Dehumidifier
                sub_button:
                  - icon: mdi:chart-line
                    entity: sensor.smart_plug_19_month_energy
                    show_state: true
                    show_icon: true
                styles: |2-

                    .bubble-icon {
                      color: rgb(169, 169, 169) !important;
                    }

                   
                    .bubble-sub-button-1 {
                      background-color: black !important;
                    }

                    
                    .bubble-button-card-container {
                      background: rgba(169,169,169,0.2) !important;
                    }
              - type: custom:bubble-card
                card_type: button
                button_type: state
                entity: sensor.12_smart_plug_current_power
                name: Washing Machine
                sub_button:
                  - icon: mdi:chart-line
                    entity: sensor.12_smart_plug_month_energy
                    show_state: true
                    show_icon: true
                styles: |2-

                    .bubble-icon {
                      color: rgb(169, 169, 169) !important;
                    }

                   
                    .bubble-sub-button-1 {
                      background-color: black !important;
                    }

                    
                    .bubble-button-card-container {
                      background: rgba(169,169,169,0.2) !important;
                    }
              - type: custom:bubble-card
                card_type: button
                button_type: state
                entity: sensor.9_smart_plug_current_power
                name: Dishwasher
                sub_button:
                  - icon: mdi:chart-line
                    entity: sensor.9_smart_plug_month_energy
                    show_state: true
                    show_icon: true
                styles: |2-

                    .bubble-icon {
                      color: rgb(169, 169, 169) !important;
                    }

                   
                    .bubble-sub-button-1 {
                      background-color: black !important;
                    }

                    
                    .bubble-button-card-container {
                      background: rgba(169,169,169,0.2) !important;
                    }
              - type: custom:bubble-card
                card_type: button
                button_type: state
                entity: sensor.13_smart_plug_current_power
                name: Lounge TV
                sub_button:
                  - icon: mdi:chart-line
                    entity: sensor.13_smart_plug_month_energy
                    show_state: true
                    show_icon: true
                styles: |2-

                    .bubble-icon {
                      color: rgb(255, 215, 0) !important;
                    }

                   
                    .bubble-sub-button-1 {
                      background-color: black !important;
                    }

                    
                    .bubble-button-card-container {
                      background: rgb(255, 215, 100, 0.2) !important;
                    }
```
