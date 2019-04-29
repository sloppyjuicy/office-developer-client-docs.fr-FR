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
  
Décrit un contrôle qui sera utilisé dans une boîte de dialogue construite à partir d'une table d'affichage. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
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
  
> Type de contrôle inclus dans le membre **CTL** et correspondant à la propriété **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) du contrôle. Les valeurs possibles sont les suivantes:
    
DTCT_LABEL 
  
> Contrôle Étiquette
    
DTCT_EDIT 
  
> Contrôle d'édition.
    
DTCT_LBX 
  
> Contrôle zone de liste.
    
DTCT_COMBOBOX 
  
> Contrôle de zone de liste déRoulante.
    
DTCT_DDLBX 
  
> Contrôle de liste déRoulante.
    
DTCT_CHECKBOX 
  
> Contrôle case à coCher.
    
DTCT_GROUPBOX 
  
> Contrôle de zone de groupe.
    
DTCT_BUTTON 
  
> Contrôle bouton.
    
DTCT_PAGE 
  
> Contrôle page à onglets.
    
DTCT_RADIOBUTTON 
  
> Contrôle de case d'option.
    
DTCT_MVLISTBOX 
  
> Contrôle de liste à valeurs multiples.
    
DTCT_MVDDLBX 
  
> Contrôle de liste déroulante à valeurs multiples.
    
**ulCtlFlags**
  
> Masque de des indicateurs qui décrit les fonctionnalités du contrôle et correspond à la propriété **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) du contrôle. Ces indicateurs peuvent être définis pour les cases à cocher, les zones de liste déroulante, les zones de liste et les contrôles d'édition uniquement. Les valeurs possibles sont les suivantes:
    
DT_ACCEPT_DBCS 
  
> Le format ANSI ou DBCS est accepté. Cet indicateur est valide uniquement pour les contrôles d'édition.
    
DT_EDITABLE 
  
> Un utilisateur peut modifier le texte dans le contrôle. 
    
DT_MULTILINE 
  
> Le contrôle peut contenir plusieurs lignes de texte. Cet indicateur est valide uniquement pour les contrôles d'édition.
    
DT_PASSWORD_EDIT 
  
> Le contrôle contient un mot de passe; par conséquent, le contenu du contrôle ne doit pas être affiché à l'utilisateur. Cet indicateur est valide uniquement pour les contrôles d'édition.
    
DT_REQUIRED 
  
> Le contrôle de la boîte de dialogue est obligatoire. Cet indicateur est valide uniquement pour les contrôles de zone de liste modifiable et de modification.
    
DT_SET_IMMEDIATE 
  
> Active la sortie immédiate d'une valeur lors d'une modification dans le contrôle. Cela permet d'établir une relation de dépendance entre deux contrôles. 
    
**lpbNotif**
  
> Pointeur vers une structure qui se compose d'une structure de [GUID](guid.md) , pour représenter le fournisseur de services et un identificateur pour le contrôle. Les membres **lpbNotif** et **cbNotif** correspondent à la propriété **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) du contrôle et sont utilisés pour avertir l'interface utilisateur lorsque le contrôle doit être mis à jour.
    
**cbNotif**
  
> Nombre d'octets dans la structure vers laquelle pointe le membre **lpbNotif** . 
    
**lpszFilter**
  
> Pointeur vers une chaîne de caractères qui décrit quels caractères peuvent être saisis dans un contrôle de zone de liste modifiable ou de modification. Pour les autres types de contrôles, le membre **lpszFilter** peut être null. Pour les contrôles de zone de liste modifiable et de zone de liste modifiable, il doit s'agir d'une expression régulière qui s'applique à un seul caractère à la fois. Le même filtre est appliqué à tous les caractères dans le contrôle. Le format de la chaîne de filtrage est le suivant: 
    
|**Caractère**|**Description**|
|:-----|:-----|
| `*` <br/> | N'importe quel caractère est autorisé (par `"*"`exemple,).  <br/> |
| `[ ]` <br/> |Définit un jeu de caractères (par exemple, `"[0123456789]"`.)  <br/> |
| `-` <br/> |Indique une plage de caractères (par exemple, `"[a-z]"`).  <br/> |
| `~` <br/> |Indique que ces caractères ne sont pas autorisés (par exemple `"[~0-9]")`,. <br/>|   
| `\` <br/> |Utilisé pour citer tous les symboles précédents (par exemple, `"[\-\\\[\]]"` les caractères «, \, » et «») sont autorisés.  <br/> |
   
**ulItemID**
  
> Valeur qui identifie le contrôle dans la ressource de la boîte de dialogue. Pour les contrôles de pages à onglets de type DTCT_PAGE, le membre **ulItemID** est éventuellement utilisé pour charger le nom du composant de la page à partir d'une ressource de type chaîne. Les informations sur la position et l'étiquette sont lues à partir de la ressource de la boîte de dialogue. 
    
**CTL**
  
> Structure qui contient les données du contrôle et correspond à la propriété **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) du contrôle. Chaque type de contrôle a une structure différente.
    
## <a name="remarks"></a>Remarques

La structure **DTCTL** décrit un contrôle de n'importe quel type. La plupart de ses membres sont utilisés pour définir des propriétés sur le contrôle. 
  
Le membre **CTL** est une Union de structures qui se rapportent à un type de contrôle particulier. Si la structure **DTCTL** décrit un contrôle d'édition, par exemple, le membre de la **liste de certificats de confiance** pointe vers une structure [DTBLEDIT](dtbledit.md) . Cette structure correspond à la propriété **PR_CONTROL_STRUCTURE** du contrôle. L'Union a comme premier membre une variable de type LPVOID pour permettre l'initialisation au moment de la compilation de la structure **DTCTL** . 
  
Bien que la fonction [BuildDisplayTable](builddisplaytable.md) utilise la structure **DTCTL** pour créer la table d'affichage à partir des ressources de contrôle, la structure **DTCTL** n'apparaît jamais dans le tableau d'affichage proprement dit. Cette structure fournit des informations à **BuildDisplayTable**.
  
Dans le membre **ulCtlFlags** , quatre indicateurs DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT affectent uniquement les contrôles d'édition. Deux autres DT_REQUIRED et DT_SET_IMMEDIATE affectent tous les contrôles modifiables. 
  
Les contrôles disponibles pour une boîte de dialogue sont étiquette, zone de texte, zone de texte prenant en charge l'entrée manuscrite, liste, liste déroulante, zone de liste déroulante, zone de groupe, bouton, case d'option et page à onglets.
  
Pour une vue d'ensemble des tables d'affichage, voir [afficher les tables](display-tables.md). Pour plus d'informations sur l'implémentation d'une table d'affichage, voir [Implementing a Display table](display-table-implementation.md).
  
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

