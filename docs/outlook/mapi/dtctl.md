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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 1ce379ac70f140aae24880b118ca7293f2e72aa4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574712"
---
# <a name="dtctl"></a>DTCTL

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décrit un contrôle qui sera utilisé dans une boîte de dialogue établie à partir d’un tableau d’affichage. 
  
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
  
> Type de contrôle qui est inclus dans le membre de **confiance** et correspond à la propriété **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) du contrôle. Les valeurs possibles sont les suivantes :
    
DTCT_LABEL 
  
> Contrôle Étiquette
    
DTCT_EDIT 
  
> Contrôle d’édition.
    
DTCT_LBX 
  
> Contrôle zone de liste.
    
DTCT_COMBOBOX 
  
> Contrôle zone de liste déroulante.
    
DTCT_DDLBX 
  
> Contrôle de liste déroulante.
    
DTCT_CHECKBOX 
  
> Contrôle case à cocher.
    
DTCT_GROUPBOX 
  
> Contrôle de zone de groupe.
    
DTCT_BUTTON 
  
> Contrôle bouton.
    
DTCT_PAGE 
  
> Contrôle de la page à onglets.
    
DTCT_RADIOBUTTON 
  
> Contrôle case d’option.
    
DTCT_MVLISTBOX 
  
> Contrôle de liste à valeurs multiples.
    
DTCT_MVDDLBX 
  
> Contrôle de liste déroulante à valeurs multiples.
    
**ulCtlFlags**
  
> Masque de bits d’indicateurs qui décrit les fonctionnalités du contrôle et correspond à la propriété **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) du contrôle. Ces indicateurs peuvent être définies pour les cases à cocher, les zones de liste déroulante, les zones de liste et uniquement les contrôles d’édition. Les valeurs possibles sont les suivantes :
    
DT_ACCEPT_DBCS 
  
> Format de l’ANSI ou DBCS est accepté. Cet indicateur n’est valide que pour les contrôles d’édition.
    
DT_EDITABLE 
  
> Un utilisateur peut modifier le texte dans le contrôle. 
    
DT_MULTILINE 
  
> Le contrôle peut contenir plusieurs lignes de texte. Cet indicateur n’est valide que pour les contrôles d’édition.
    
DT_PASSWORD_EDIT 
  
> Le contrôle contient un mot de passe ; Par conséquent, le contenu du contrôle ne doit pas être affiché à l’utilisateur. Cet indicateur n’est valide que pour les contrôles d’édition.
    
DT_REQUIRED 
  
> Le contrôle de boîte de dialogue est requis. Cet indicateur n’est valide uniquement pour les contrôles de zone de liste déroulante et de modifier.
    
DT_SET_IMMEDIATE 
  
> Active la sortie immédiate d’une valeur à une modification dans le contrôle. Cela permet une relation de dépendance être établie entre deux contrôles. 
    
**lpbNotif**
  
> Pointeur vers une structure qui se compose d’une structure [GUID](guid.md) , pour représenter le fournisseur de services et un identificateur pour le contrôle. Les membres **lpbNotif** et **cbNotif** correspondant à la propriété du contrôle **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) et sont utilisés pour avertir l’interface utilisateur lorsque le contrôle doit être mis à jour.
    
**cbNotif**
  
> Nombre d’octets de la structure vers laquelle pointe le membre **lpbNotif** . 
    
**lpszFilter**
  
> Pointeur vers une chaîne de caractères qui décrit les caractères qui peut être saisi dans un contrôle de zone de liste déroulante ou de modifier. Pour d’autres types de contrôles, le membre **lpszFilter** peut être NULL. Pour les contrôles de zone de liste déroulante et de modifier, il doit être une expression régulière qui s’applique à un seul caractère à la fois. Le même filtre est appliqué à tous les caractères dans le contrôle. Le format de la chaîne de filtre est comme suit : 
    
|**Caractère**|**Description**|
|:-----|:-----|
| `*` <br/> | N’importe quel caractère est autorisé (par exemple, `"*"`).  <br/> |
| `[ ]` <br/> |Définit un jeu de caractères (par exemple, `"[0123456789]"`.)  <br/> |
| `-` <br/> |Indique une plage de caractères (par exemple, `"[a-z]"`).  <br/> |
| `~` <br/> |Indique que ces caractères ne sont pas autorisés (par exemple, `"[~0-9]")`. <br/>|   
| `\` <br/> |Utilisé pour les symboles précédentes quote (par exemple, `"[\-\\\[\]]"` signifie-, \, [, et] caractères sont autorisés).  <br/> |
   
**ulItemID**
  
> Valeur qui identifie le contrôle de la ressource de boîte de dialogue. Pour les contrôles des pages à onglets de type DTCT_PAGE **ulItemID** membre (facultatif) permet de charger le nom du composant de la page à partir d’une ressource de chaîne. Obtenir des informations de l’étiquette et position sont lues à partir de la ressource de boîte de dialogue. 
    
**confiance**
  
> Structure qui conserve les données du contrôle et correspond à la propriété **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) du contrôle. Chaque type de contrôle possède une structure différente.
    
## <a name="remarks"></a>Remarques

La structure **DTCTL** décrit un contrôle quelconque. La plupart de ses membres sont utilisés pour définir les propriétés sur le contrôle. 
  
Le membre de **confiance** est union de structures qui sont associées à un type particulier de contrôle. Si la structure **DTCTL** est décrivant un contrôle d’édition, par exemple, le membre de **confiance** pointe vers une structure [DTBLEDIT](dtbledit.md) . Cette structure correspond à la propriété **PR_CONTROL_STRUCTURE** du contrôle. L’union dispose d’une variable de type LPVOID pour permettre l’initialisation de temps de compilation de la structure **DTCTL** en premier membre. 
  
Bien que la fonction [BuildDisplayTable](builddisplaytable.md) utilise la structure **DTCTL** pour la création de la table d’affichage de ressources du contrôle, la structure **DTCTL** n’apparaît jamais dans la table d’affichage lui-même. Cette structure fournit uniquement des informations à **BuildDisplayTable**.
  
Dans le membre **ulCtlFlags** , quatre indicateurs DT_ACCEPT_DBCS, DT_EDITABLE, effet DT_MULTILINE_and DT_PASSWORD_EDIT uniquement les contrôles d’édition. Deux autres DT_REQUIRED et DT_SET_IMMEDIATE affectent tous les contrôles modifiables. 
  
Les contrôles disponibles pour une boîte de dialogue sont étiquette, zone de texte, zone de texte prenant en charge les entrées manuscrites, liste, liste déroulante, zone de liste déroulante, case à cocher, zone de groupe, bouton, case d’option et page à onglets.
  
Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md). Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).
  
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

