# PID-VLA Mesh Generation Prompts Reference

**Docset-wide final solution:** `cobot-atlas README.md` §A.8 is the decision record. These prompts are auxiliary asset-generation inputs, not scientific evidence by themselves; any generated output used in experiments must be logged with prompt/config hashes, provider/version metadata, and license/provenance.

This document lists all 23 meshes required for the PID-VLA simulation environment with detailed prompts for generation.

---

## Category: Manipulation Objects

### 1. red_cube
**Purpose:** Primary manipulation target for pick-and-place experiments (Exp1, Exp2)  
**Dimensions:** 5x5x5 cm cube  
**Physics:** cuboid, 0.1 kg  
**Material:** plastic_red

**Image Prompt:**
> Solid red matte plastic cube toy block, clean edges, photorealistic rendering, white studio background, soft shadows

**Text Prompt:**
> A simple solid red plastic cube, 5cm on each side, matte finish, photorealistic, product photography style, clean white background, studio lighting, no shadows on background

---

### 2. blue_cube
**Purpose:** Stacking experiments (Exp2) - middle layer  
**Dimensions:** 5x5x5 cm cube  
**Physics:** cuboid, 0.1 kg  
**Material:** plastic_blue

**Image Prompt:**
> Solid blue matte plastic cube toy block, clean edges, photorealistic rendering, white studio background, soft shadows

**Text Prompt:**
> A simple solid blue plastic cube, 5cm on each side, matte finish, photorealistic, product photography style, clean white background, studio lighting

---

### 3. green_cube
**Purpose:** Stacking experiments (Exp2) - top layer  
**Dimensions:** 5x5x5 cm cube  
**Physics:** cuboid, 0.1 kg  
**Material:** plastic_green

**Image Prompt:**
> Solid green matte plastic cube toy block, clean edges, photorealistic rendering, white studio background, soft shadows

**Text Prompt:**
> A simple solid green plastic cube, 5cm on each side, matte finish, photorealistic, product photography style, clean white background, studio lighting

---

### 4. blue_cylinder
**Purpose:** Distractor object and manipulation target  
**Dimensions:** radius 3cm, height 8cm  
**Physics:** cylinder, 0.15 kg  
**Material:** plastic_blue

**Image Prompt:**
> Blue matte plastic cylinder standing upright, 8cm tall 6cm diameter, photorealistic rendering, white studio background

**Text Prompt:**
> A solid blue plastic cylinder, 3cm radius and 8cm tall, matte finish, photorealistic, product photography, clean white background, studio lighting

---

### 5. green_sphere
**Purpose:** Spherical manipulation target for grasping experiments  
**Dimensions:** radius 4cm  
**Physics:** ball, 0.2 kg  
**Material:** plastic_green

**Image Prompt:**
> Green matte plastic ball sphere, 8cm diameter, photorealistic rendering, white studio background, soft shadows

**Text Prompt:**
> A solid green plastic sphere, 4cm radius (8cm diameter), matte finish, photorealistic, product photography, clean white background, studio lighting

---

### 6. wooden_block_A
**Purpose:** Stacking base for assembly experiments  
**Dimensions:** 10x5x3 cm rectangular block  
**Physics:** cuboid, 0.12 kg  
**Material:** wood_natural

**Image Prompt:**
> Natural wooden rectangular block, light oak wood grain texture, 10x5x3cm, photorealistic rendering, white studio background

**Text Prompt:**
> A natural wood rectangular block, 10cm x 5cm x 3cm, light oak color, visible wood grain, photorealistic, product photography, clean white background, studio lighting

---

### 7. wooden_block_B
**Purpose:** Mid-level stacking block  
**Dimensions:** 8x4x4 cm rectangular block  
**Physics:** cuboid, 0.1 kg  
**Material:** wood_natural

**Image Prompt:**
> Natural wooden block, light oak wood grain texture, 8x4x4cm, photorealistic rendering, white studio background

**Text Prompt:**
> A natural wood rectangular block, 8cm x 4cm x 4cm, light oak color, visible wood grain, photorealistic, product photography, clean white background, studio lighting

---

### 8. ycb_mustard
**Purpose:** YCB benchmark object for real-world manipulation comparison  
**Dimensions:** 19x6x6 cm bottle shape  
**Physics:** convex_hull, 0.6 kg  
**Material:** plastic_yellow

**Image Prompt:**
> Yellow plastic mustard squeeze bottle, French's mustard style, 19cm tall, photorealistic product shot, white studio background

**Text Prompt:**
> A yellow plastic mustard squeeze bottle, realistic YCB dataset style, 19cm tall, product photography, clean white background, studio lighting, photorealistic

---

### 9. ycb_spam
**Purpose:** YCB benchmark object, distractor  
**Dimensions:** 9x8x6 cm rectangular can  
**Physics:** cuboid, 0.35 kg  
**Material:** metal_can

**Image Prompt:**
> SPAM canned meat tin, blue and yellow packaging, rectangular shape, photorealistic product shot, white studio background

**Text Prompt:**
> A SPAM canned meat rectangular tin, 9x8x6cm, realistic product packaging, product photography, clean white background, studio lighting, photorealistic

---

## Category: YCB Objects

### 10. ycb_bowl
**Purpose:** YCB benchmark object, containment target  
**Dimensions:** radius 8cm, height 5cm  
**Physics:** trimesh, 0.18 kg  
**Material:** ceramic_white

**Image Prompt:**
> White ceramic bowl, simple round shape, 16cm diameter 5cm deep, matte finish, photorealistic rendering, white studio background

**Text Prompt:**
> A simple white ceramic bowl, 16cm diameter and 5cm deep, smooth matte finish, product photography, clean white background, studio lighting, photorealistic

---

## Category: Target Surfaces

### 11. blue_plate
**Purpose:** Placement target for pick-and-place experiments  
**Dimensions:** radius 10cm, height 1cm  
**Physics:** cylinder, 0.25 kg  
**Material:** ceramic_blue

**Image Prompt:**
> Blue ceramic dinner plate, flat circular, 20cm diameter, matte glaze, photorealistic rendering, white studio background

**Text Prompt:**
> A flat circular blue ceramic plate, 20cm diameter and 1cm thick, matte glaze finish, photorealistic, product photography, clean white background, studio lighting

---

### 12. target_platform
**Purpose:** Standard placement target platform  
**Dimensions:** 8x8x1 cm square platform  
**Physics:** cuboid, 0.02 kg  
**Material:** plastic_matte_gray

**Image Prompt:**
> Flat square gray plastic platform tile, 8x8x1cm, matte finish, neutral gray, photorealistic, white background

**Text Prompt:**
> A flat square gray matte plastic platform, 8cm x 8cm and 1cm thick, neutral gray color, product photography, clean white background, studio lighting

---

### 13. red_zone_marker
**Purpose:** Visual target zone for sorting experiments  
**Dimensions:** radius 8cm, height 0.1cm  
**Physics:** cylinder, 0.01 kg  
**Material:** plastic_red_translucent

**Image Prompt:**
> Flat circular red translucent acrylic disc, 16cm diameter, very thin 1mm, semi-transparent, white background

**Text Prompt:**
> A flat circular red translucent plastic marker disc, 16cm diameter and 1mm thick, semi-transparent red, product photography, clean white background

---

### 14. blue_zone_marker
**Purpose:** Visual target zone for sorting experiments  
**Dimensions:** radius 8cm, height 0.1cm  
**Physics:** cylinder, 0.01 kg  
**Material:** plastic_blue_translucent

**Image Prompt:**
> Flat circular blue translucent acrylic disc, 16cm diameter, very thin 1mm, semi-transparent, white background

**Text Prompt:**
> A flat circular blue translucent plastic marker disc, 16cm diameter and 1mm thick, semi-transparent blue, product photography, clean white background

---

### 15. target_marker
**Purpose:** Generic stacking target marker  
**Dimensions:** radius 4cm, height 0.1cm  
**Physics:** cylinder, 0.005 kg  
**Material:** plastic_gray_matte

**Image Prompt:**
> Flat circular gray matte plastic disc marker, 8cm diameter, very thin, neutral gray, white background

**Text Prompt:**
> A flat circular gray matte plastic marker disc, 8cm diameter and 1mm thick, neutral gray color, product photography, clean white background

---

## Category: Novel Geometry (Exp7)

### 16. hollow_cylinder
**Purpose:** Novel geometry challenge for Exp7 - hollow tube for peg insertion  
**Dimensions:** outer radius 3cm, inner radius 2cm, height 8cm  
**Physics:** compound_cylinder, 0.08 kg  
**Material:** plastic_orange

**Image Prompt:**
> Orange plastic hollow cylinder tube, pipe-like with visible hole through center, 6cm outer 4cm inner diameter, 8cm tall, photorealistic, white background

**Text Prompt:**
> An orange plastic hollow tube/cylinder, outer diameter 6cm, inner hole 4cm, 8cm tall, like a pipe section, product photography, clean white background, studio lighting

---

### 17. dice_cup
**Purpose:** Containment target for weighted die (Exp7)  
**Dimensions:** outer radius 4cm, height 6cm, open top  
**Physics:** trimesh, 0.05 kg  
**Material:** leather_brown

**Image Prompt:**
> Brown leather dice shaker cup, classic bar style, 8cm diameter 6cm tall, open top, photorealistic, white studio background

**Text Prompt:**
> A brown leather dice cup, 8cm diameter and 6cm tall, open at top, classic bar dice cup style, product photography, clean white background, studio lighting

---

### 18. l_block
**Purpose:** Compound geometry grasp planning challenge (Exp7)  
**Dimensions:** L-shaped: 8x4x4cm horizontal + 4x4x8cm vertical  
**Physics:** compound_cuboid, 0.15 kg  
**Material:** wood_natural

**Image Prompt:**
> L-shaped natural wooden block, light oak color, two perpendicular rectangular pieces forming L shape, photorealistic, white studio background

**Text Prompt:**
> An L-shaped wooden block, natural oak wood, formed from two rectangular pieces joined at right angle, total size approximately 8x8x4cm, product photography, clean white background

---

### 19. metal_peg
**Purpose:** Precision alignment target for hollow cylinder insertion  
**Dimensions:** radius 1.5cm, height 6cm  
**Physics:** cylinder, 0.3 kg  
**Material:** metal_steel

**Image Prompt:**
> Polished steel metal cylindrical peg, shiny chrome finish, 3cm diameter 6cm tall, photorealistic, white studio background

**Text Prompt:**
> A polished steel metal peg/cylinder, 3cm diameter and 6cm tall, shiny metallic surface, industrial look, product photography, clean white background, studio lighting

---

### 20. glass_cube
**Purpose:** Transparent object physics proxy challenge (Exp7)  
**Dimensions:** 6x6x6 cm cube  
**Physics:** cuboid, 0.25 kg  
**Material:** glass_transparent

**Image Prompt:**
> Clear transparent glass cube paperweight, 6cm sides, visible edges and refraction, photorealistic, white studio background with caustics

**Text Prompt:**
> A transparent glass cube, 6cm on each side, clear glass with visible edges and slight refraction, product photography, clean white background, studio lighting

---

## Category: Environment

### 21. tabletop_scene
**Purpose:** Primary environment - lab table surface  
**Dimensions:** 120x80x75 cm table  
**Physics:** static_mesh  
**Material:** wood_oak_laminate

**Image Prompt:**
> Modern laboratory work table, light oak laminate top 120x80cm, metal frame legs, 75cm height, photorealistic, clean studio setting

**Text Prompt:**
> A standard laboratory table, 120cm x 80cm surface, 75cm tall, light oak wood laminate top with metal legs, clean modern style, product photography, clean white background

---

## Category: Robot Parts

### 22. franka_panda_gripper
**Purpose:** Franka Panda robot gripper for manipulation  
**Dimensions:** standard Franka gripper  
**Physics:** compound_mesh  
**Material:** metal_white_plastic

**Image Prompt:**
> Franka Panda robot gripper end-effector, white plastic and metal, two-finger parallel gripper, industrial robot part, photorealistic, white background

**Text Prompt:**
> A Franka Emika Panda robot parallel gripper, white and gray industrial robot end-effector, two finger gripper, product photography, clean white background

---

## Category: Perturbation

### 23. black_panel_occluder
**Purpose:** Floating occluder for visual perturbation experiments  
**Dimensions:** 20x20x0.5 cm flat panel  
**Physics:** cuboid, 0.05 kg  
**Material:** plastic_matte_black

**Image Prompt:**
> Flat square matte black plastic panel, 20x20cm, thin 5mm, solid black, photorealistic, gray background

**Text Prompt:**
> A flat square black matte plastic panel, 20cm x 20cm and 0.5cm thick, solid black color, product photography, clean gray background

---

## Generation Tips

### For Best Results:

1. **Always include:** "photorealistic, product photography, clean white background, studio lighting"

2. **For simple shapes:** Be explicit about dimensions and finish (matte/glossy)

3. **For YCB objects:** Reference the actual product for authentic appearance

4. **For transparent objects:** Include "visible edges, refraction, caustics"

5. **For wood textures:** Specify "visible wood grain, light oak/walnut color"

6. **For metal objects:** Specify finish - "polished/brushed/matte, chrome/steel/aluminum"

### Common Issues:

- **Too detailed backgrounds:** Add "no shadows on background, isolated object"
- **Wrong scale perception:** Include human-relatable size reference in prompt
- **Missing features:** Be explicit about holes, openings, internal structure
