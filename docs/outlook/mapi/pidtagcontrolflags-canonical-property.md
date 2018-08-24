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
ms.openlocfilehash: fc47dc88ed0618bcdf46c309776d5a871d2128e9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580739"
---
# <a name="pidtagcontrolflags-canonical-property"></a>Propriété canonique PidTagControlFlags

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un masque de bits d’indicateurs régissant le comportement d’un contrôle utilisé dans une boîte de dialogue établie à partir d’un tableau d’affichage.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTROL_FLAGS  <br/> |
|Identificateur :  <br/> |0x3F00  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Afficher une table MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Un ou plusieurs des indicateurs suivants peuvent être définie pour cette propriété :
  
DT_ACCEPT_DBCS 
  
> Le contrôle peut contenir des caractères de définir de caractères codés sur deux octets (DBCS) qu’il contient. Cet indicateur est utilisé avec les contrôles d’édition. Il permet de jeux de caractères codés sur plusieurs.
    
DT_EDITABLE 
  
> Le contrôle peut être modifié ; la valeur associée au contrôle peut être modifiée. Lorsque cet indicateur n’est pas défini, le contrôle est en lecture seule. Cette valeur est ignorée sur l’étiquette, zone de groupe, bouton de commande standard, à valeurs multiples de liste déroulante zone de liste et les contrôles de zone de liste.
    
DT_MULTILINE 
  
> Le contrôle d’édition peut contenir plusieurs lignes. Cela signifie qu'un caractère de retour peut être entré dans le contrôle. Cet indicateur n’est valide que pour les contrôles d’édition.
    
DT_PASSWORD_EDIT 
  
> S’applique aux contrôles d’édition. Le contrôle d’édition est traité comme un mot de passe. La valeur est affichée à l’aide d’astérisques au lieu de la résonance des caractères entrés.
    
DT_REQUIRED 
  
> Si le contrôle autorise les modifications (DT_EDITABLE), il doit avoir une valeur [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appelée. 
    
DT_SET_IMMEDIATE 
  
> Active un paramètre exécution d’une valeur ; dès qu’une valeur dans le contrôle change, MAPI appelle la méthode **SetProps** pour la propriété associée à ce contrôle. Lorsque cet indicateur n’est pas défini, les valeurs sont définies lorsque la boîte de dialogue est fermée. 
    
DT_SET_SELECTION 
  
> Lorsqu’une sélection est effectuée dans la zone de liste, la colonne de l’index de cette zone de liste est définie en tant que propriété. Toujours utilisé avec DT_SET_IMMEDIATE.
    
Cette propriété est stockée dans le membre ulCtlFlags de structure de [DTCTL](dtctl.md) d’un contrôle. La plupart des indicateurs de contrôle qui s’appliquent à tous les contrôles qui autorisent les entrées utilisateur ; quelques-unes s’appliquent uniquement au contrôle d’édition. Les contrôles qui n’autorisent pas l’entrée de l’utilisateur, par exemple un bouton ou une étiquette, la valeur 0 pour les indicateurs de contrôle. 
  
La plupart des valeurs d’indicateur sont explicites. Par exemple, lorsque DT_REQUIRED est définie pour un contrôle, il doit contenir une valeur avant de la boîte de dialogue est autorisée à être fermée. Le fournisseur de services peut fournir une valeur via son implémentation **IMAPIProp** ou l’utilisateur peut entrer un. DT_EDITABLE indique que la valeur du contrôle peut être modifiée. DT_MULTILINE permet à la valeur d’un contrôle d’édition de couvrir plusieurs lignes. 
  
Certains indicateurs de contrôle ne sont pas évidentes dans leur signification. Lorsqu’un contrôle définit l’indicateur DT_SET_IMMEDIATE, les modifications à prendre de sa valeur affectent dès que l’utilisateur déplace vers un nouveau contrôle. MAPI permet à un seul appel à la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de l’interface propriété pour la propriété du contrôle. Cela diffère le comportement par défaut, qui consiste à différer ayant des modifications apportées aux valeurs de contrôle prendront effet qu’après que l’utilisateur sélectionne le bouton **OK** ou ferme la boîte de dialogue. L’indicateur DT_SET_IMMEDIATE est souvent utilisée en combinaison avec afficher les notifications de table. 
  
Le tableau suivant répertorie les types de contrôles et toutes les valeurs d’indicateur qui peuvent être définies pour chaque type.
  
|**Contrôle**|**Valeurs valides pour cette propriété**|
|:-----|:-----|
|Bouton  <br/> |Doit être égal à zéro  <br/> |
|Case à cocher  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Zone de liste modifiable  <br/> |DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Zone de liste déroulante  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Modifier  <br/> |DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Zone de groupe  <br/> |Doit être égal à zéro  <br/> |
|Étiquette  <br/> |Doit être égal à zéro  <br/> |
|Zone de liste  <br/> |Doit être égal à zéro  <br/> |
|Zone de liste déroulante à valeurs multiples  <br/> |Doit être égal à zéro  <br/> |
|Zone de liste à valeurs multiples  <br/> |Doit être égal à zéro  <br/> |
|Page à onglets  <br/> |Doit être égal à zéro  <br/> |
|Case d’option  <br/> |Doit être égal à zéro  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

