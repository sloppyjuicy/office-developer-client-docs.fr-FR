---
title: DTCTL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTCTL
api_type:
- COM
ms.assetid: 6d1589e9-b171-427a-9a3e-b4154ee8ceb6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2a2ca1fba5dceb45b41c2f25a96e163f02c41440
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421500"
---
# <a name="dtctl"></a>DTCTL

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit un contrôle qui sera utilisé dans une boîte de dialogue conçue à partir d’un tableau d’affichage. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG ulCtlType;
  ULONG ulCtlFlags;
  LPBYTE lpbNotif;
  ULONG cbNotif;
  LPSTR lpszFilter;
  ULONG ulItemID;
  union
  {
    LPVOID lpv;
    LPDTBLLABEL lplabel;
    LPDTBLEDIT lpedit;
    LPDTBLLBX lplbx;
    LPDTBLCOMBOBOX lpcombobox;
    LPDTBLDDLBX lpddlbx;
    LPDTBLCHECKBOX lpcheckbox;
    LPDTBLGROUPBOX lpgroupbox;
    LPDTBLBUTTON lpbutton;
    LPDTBLRADIOBUTTON lpradiobutton;
    LPDTBLMVLISTBOX lpmvlbx;
    LPDTBLMVDDLBX lpmvddlbx;
    LPDTBLPAGE lppage;
  } ctl;
} DTCTL, FAR *LPDTCTL;

```

## <a name="members"></a>Members

**ulCtlType**
  
> Type de contrôle qui est inclus dans le membre **ctl** et correspond à la propriété PR_CONTROL_TYPE **(** [PidTagControlType](pidtagcontroltype-canonical-property.md)) du contrôle. Les valeurs possibles sont les suivantes :
    
DTCT_LABEL 
  
> Contrôle Étiquette
    
DTCT_EDIT 
  
> Contrôle d’édition.
    
DTCT_LBX 
  
> Contrôle Zone de liste.
    
DTCT_COMBOBOX 
  
> Contrôle Zone de liste déroulante.
    
DTCT_DDLBX 
  
> Contrôle de liste liste de listes.
    
DTCT_CHECKBOX 
  
> Contrôle Case à cocher.
    
DTCT_GROUPBOX 
  
> Contrôle zone de groupe.
    
DTCT_BUTTON 
  
> Contrôle bouton.
    
DTCT_PAGE 
  
> Contrôle de page à onglets.
    
DTCT_RADIOBUTTON 
  
> Contrôle de bouton d’radio.
    
DTCT_MVLISTBOX 
  
> Contrôle de liste à valeurs multiples.
    
DTCT_MVDDLBX 
  
> Contrôle de listes de listes listes à valeurs multiples.
    
**ulCtlFlags**
  
> Masque de bits d’indicateurs qui décrit les fonctionnalités du contrôle et correspond à la propriété **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)). Ces indicateurs peuvent être définies pour les cases à cocher, les zones de liste déroulante, les zones de liste et les contrôles de modification uniquement. Les valeurs possibles sont les suivantes :
    
DT_ACCEPT_DBCS 
  
> Le format ANSI ou DBCS est accepté. Cet indicateur est valide pour les contrôles d’édition uniquement.
    
DT_EDITABLE 
  
> Un utilisateur peut modifier le texte du contrôle. 
    
DT_MULTILINE 
  
> Le contrôle peut contenir plusieurs lignes de texte. Cet indicateur est valide pour les contrôles d’édition uniquement.
    
DT_PASSWORD_EDIT 
  
> Le contrôle contient un mot de passe ; par conséquent, le contenu du contrôle ne doit pas être affiché à l’utilisateur. Cet indicateur est valide pour les contrôles d’édition uniquement.
    
DT_REQUIRED 
  
> Le contrôle de boîte de dialogue est obligatoire. Cet indicateur est valide uniquement pour les contrôles de zone de liste modifiable et de modification.
    
DT_SET_IMMEDIATE 
  
> Active la sortie immédiate d’une valeur en cas de modification du contrôle. Cela permet d’établir une relation de dépendance entre deux contrôles. 
    
**lpbNotif**
  
> Pointeur vers une structure constituée d’une structure [GUID,](guid.md) pour représenter le fournisseur de services et un identificateur pour le contrôle. Les membres **lpbNotif** et **cbNotif** correspondent à la propriété **PR_CONTROL_ID (** [PidTagControlId](pidtagcontrolid-canonical-property.md)) du contrôle et sont utilisés pour avertir l’interface utilisateur lorsque le contrôle doit être mis à jour.
    
**cbNotif**
  
> Nombre d’octets dans la structure pointée par **le membre lpbNotif.** 
    
**lpszFilter**
  
> Pointeur vers une chaîne de caractères qui décrit les caractères qui peuvent être entrés dans un contrôle de zone de liste modifiable ou modifiable. Pour d’autres types de contrôles, le **membre lpszFilter** peut être NULL. Pour les contrôles d’édition et de zone de liste déroulante, il doit s’agit d’une expression régulière qui s’applique à un seul caractère à la fois. Le même filtre est appliqué à tous les caractères du contrôle. Le format de la chaîne de filtre est le suivant : 
    
|**Caractère**|**Description**|
|:-----|:-----|
| `*` <br/> | Tout caractère est autorisé (par exemple, `"*"` ).  <br/> |
| `[ ]` <br/> |Définit un ensemble de caractères (par exemple, `"[0123456789]"` .)  <br/> |
| `-` <br/> |Indique une plage de caractères (par exemple, `"[a-z]"` ).  <br/> |
| `~` <br/> |Indique que ces caractères ne sont pas autorisés (par exemple, `"[~0-9]")` . <br/>|   
| `\` <br/> |Utilisé pour guillemets l’un des symboles précédents (par exemple, les caractères `"[\-\\\[\]]"` -, \, [et ] sont autorisés).  <br/> |
   
**ulItemID**
  
> Valeur qui identifie le contrôle dans la ressource de boîte de dialogue. Pour les contrôles de pages à onglets de type DTCT_PAGE le membre **ulItemID** est éventuellement utilisé pour charger le nom du composant de la page à partir d’une ressource de chaîne. Les informations de position et d’étiquette sont lues à partir de la ressource de la boîte de dialogue. 
    
**ctl**
  
> Structure qui contient les données du contrôle et correspond à la propriété PR_CONTROL_STRUCTURE **(** [PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)). Chaque type de contrôle a une structure différente.
    
## <a name="remarks"></a>Remarques

La structure **DTCTL** décrit un contrôle de n’importe quel type. La plupart de ses membres sont utilisés pour définir des propriétés sur le contrôle. 
  
Le **membre ctl** est une union de structures liées à un type particulier de contrôle. Si la structure **DTCTL** décrit un contrôle d’édition, par exemple, le membre **ctl** pointe vers une structure [DTBLEDIT.](dtbledit.md) Cette structure correspond à la propriété PR_CONTROL_STRUCTURE **du** contrôle. L’union possède comme premier membre une variable de type LPVOID pour permettre l’initialisation du temps de compilation de la structure **DTCTL.** 
  
Bien que la [fonction BuildDisplayTable](builddisplaytable.md) utilise la structure **DTCTL** pour créer la table d’affichage à partir des ressources de contrôle, la structure **DTCTL** n’apparaît jamais dans le tableau d’affichage lui-même. Cette structure fournit simplement des informations **à BuildDisplayTable**.
  
Dans le **membre ulCtlFlags,** quatre indicateurs DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT les contrôles d’édition uniquement. Deux autres DT_REQUIRED et DT_SET_IMMEDIATE un contrôle modifiable. 
  
Les contrôles disponibles pour une boîte de dialogue sont étiquette, zone de texte, zone de texte sensible à l’encre, liste, liste déroulante, zone de liste déroulante, case à cocher, zone de groupe, bouton, case d’radio et page à onglets.
  
Pour une vue d’ensemble des tableaux d’affichage, voir [Afficher les tableaux.](display-tables.md) Pour plus d’informations sur l’implémentation d’un tableau d’affichage, voir [Implementing a Display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi

- [BuildDisplayTable](builddisplaytable.md)
- [DTBLBUTTON](dtblbutton.md)
- [DTBLCHECKBOX](dtblcheckbox.md)
- [DTBLCOMBOBOX](dtblcombobox.md)
- [DTBLDDLBX](dtblddlbx.md)
- [DTBLEDIT](dtbledit.md)
- [DTBLGROUPBOX](dtblgroupbox.md)
- [DTBLLABEL](dtbllabel.md)
- [DTBLLBX](dtbllbx.md)
- [DTBLMVDDLBOX](dtblmvddlbox.md)
- [DTBLMVLISTBOX](dtblmvlistbox.md)
- [DTBLPAGE](dtblpage.md)
- [DTBLRADIOBUTTON](dtblradiobutton.md)
- [Structures MAPI](mapi-structures.md)

