---
title: Propriété canonique PidTagControlFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlFlags
api_type:
- HeaderDef
ms.assetid: b97a9e72-fbb7-49ab-a19d-5e9bd1b8a80d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 099f08876eadc83ebb66b9e4226eeeee6277bf01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430881"
---
# <a name="pidtagcontrolflags-canonical-property"></a>Propriété canonique PidTagControlFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de bits d’indicateurs régissant le comportement d’un contrôle utilisé dans une boîte de dialogue conçue à partir d’un tableau d’affichage.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTROL_FLAGS  <br/> |
|Identificateur :  <br/> |0x3F00  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Tableau d’affichage MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Un ou plusieurs des indicateurs suivants peuvent être définies pour cette propriété :
  
DT_ACCEPT_DBCS 
  
> Le contrôle peut être Double-Byte de jeu de caractères (DBCS). Cet indicateur est utilisé avec les contrôles d’édition. Il autorise les jeux de caractères multi-sur-deux.
    
DT_EDITABLE 
  
> Le contrôle peut être modifié . la valeur associée au contrôle peut être modifiée. Lorsque cet indicateur n’est pas définie, le contrôle est en lecture seule. Cette valeur est ignorée sur les contrôles d’étiquette, de zone de groupe, de bouton push standard, de zone de liste liste et de zone de liste à valeurs multiples.
    
DT_MULTILINE 
  
> Le contrôle d’édition peut contenir plusieurs lignes. Cela signifie qu’un caractère de retour peut être entré dans le contrôle. Cet indicateur est valide pour les contrôles d’édition uniquement.
    
DT_PASSWORD_EDIT 
  
> S’applique aux contrôles d’édition. Le contrôle d’édition est traité comme un mot de passe. La valeur est affichée à l’aide d’astérisques au lieu d’un écho des caractères réels entrés.
    
DT_REQUIRED 
  
> Si le contrôle autorise les modifications (DT_EDITABLE), il doit avoir une valeur avant d’appeler [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) 
    
DT_SET_IMMEDIATE 
  
> Active la définition immédiate d’une valeur ; Dès qu’une valeur du contrôle change, MAPI appelle la méthode **SetProps** pour la propriété associée à ce contrôle. Lorsque cet indicateur n’est pas définie, les valeurs sont définies lorsque la boîte de dialogue est rejetée. 
    
DT_SET_SELECTION 
  
> Lorsqu’une sélection est réalisée dans la zone de liste, la colonne d’index de cette zone de liste est définie en tant que propriété. Toujours utilisé avec les DT_SET_IMMEDIATE.
    
Cette propriété est stockée dans le membre ulCtlFlags de la structure [DTCTL](dtctl.md) d’un contrôle. La plupart des indicateurs de contrôle s’appliquent à tous les contrôles qui autorisent l’entrée utilisateur ; Quelques-unes s’appliquent uniquement au contrôle d’édition. Les contrôles qui n’autorisent pas l’entrée utilisateur, tels qu’un bouton ou une étiquette, définissent 0 pour leurs indicateurs de contrôle. 
  
La plupart des valeurs d’indicateur sont explicites. Par exemple, lorsque DT_REQUIRED est définie pour un contrôle, elle doit contenir une valeur avant que la boîte de dialogue ne soit autorisée à être rejetée. Le fournisseur de services peut fournir une valeur via son **implémentation IMAPIProp** ou l’utilisateur peut en entrer une. DT_EDITABLE indique que la valeur du contrôle peut être modifiée. DT_MULTILINE permet à la valeur d’un contrôle d’édition de s’étendre sur plusieurs lignes. 
  
Certains indicateurs de contrôle ne sont pas aussi évidents à comprendre. Lorsqu’un contrôle définit l’DT_SET_IMMEDIATE, les modifications apportées à sa valeur prennent effet dès que l’utilisateur passe à un nouveau contrôle. MAPI effectue un appel unique à la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de l’interface de propriétés pour la propriété du contrôle. Ce comportement est différent du comportement par défaut, qui consiste à reporter l’application des modifications apportées aux valeurs de contrôle jusqu’à ce que l’utilisateur sélectionne le bouton **OK** ou qu’il a fait disparaître la boîte de dialogue. L DT_SET_IMMEDIATE est souvent utilisé en combinaison avec les notifications du tableau d’affichage. 
  
Le tableau suivant répertorie les types de contrôles et toutes les valeurs d’indicateur qui peuvent être définies pour chaque type.
  
|**Contrôle**|**Valeurs valides pour cette propriété**|
|:-----|:-----|
|Bouton  <br/> |Doit être zéro  <br/> |
|Case à cocher  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Zone de liste modifiable  <br/> |DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Zone de liste liste  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Modifier  <br/> |DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Zone de groupe  <br/> |Doit être zéro  <br/> |
|Étiquette  <br/> |Doit être zéro  <br/> |
|Zone de liste  <br/> |Doit être zéro  <br/> |
|Zone de liste rouge à valeurs multiples  <br/> |Doit être zéro  <br/> |
|Zone de liste à valeurs multiples  <br/> |Doit être zéro  <br/> |
|Page à onglets  <br/> |Doit être zéro  <br/> |
|Bouton d’radio  <br/> |Doit être zéro  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

