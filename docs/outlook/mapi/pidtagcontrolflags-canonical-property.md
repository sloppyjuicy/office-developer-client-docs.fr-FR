---
title: Propriété canonique PidTagControlFlags
description: Décrit la propriété canonique PidTagControlFlags, qui contient un masque de bits d’indicateurs régissant le comportement d’un contrôle.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagControlFlags
api_type:
- HeaderDef
ms.assetid: b97a9e72-fbb7-49ab-a19d-5e9bd1b8a80d
ms.openlocfilehash: c64cb251132e6767b162020567a1f466c8b2465f
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770571"
---
# <a name="pidtagcontrolflags-canonical-property"></a>Propriété canonique PidTagControlFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de bits des indicateurs qui régissent le comportement d’un contrôle utilisé dans une boîte de dialogue créée à partir d’une table d’affichage.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTROL_FLAGS  <br/> |
|Identificateur :  <br/> |0x3F00  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Table d’affichage MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Un ou plusieurs des indicateurs suivants peuvent être définis pour cette propriété :
  
DT_ACCEPT_DBCS 
  
> Le contrôle peut contenir Double-Byte caractères DBCS (Character Set). Cet indicateur est utilisé avec les contrôles de modification. Il autorise les jeux de caractères sur plusieurs octets.
    
DT_EDITABLE 
  
> Le contrôle peut être modifié ; la valeur associée au contrôle peut être modifiée. Lorsque cet indicateur n’est pas défini, le contrôle est en lecture seule. Cette valeur est ignorée sur les contrôles d’étiquette, de zone de groupe, de bouton Push standard, de zone de liste déroulante à valeurs multiples et de zone de liste.
    
DT_MULTILINE 
  
> Le contrôle d’édition peut contenir plusieurs lignes. Cela signifie qu’un caractère de retour peut être entré dans le contrôle. Cet indicateur est valide uniquement pour les contrôles de modification.
    
DT_PASSWORD_EDIT 
  
> S’applique aux contrôles de modification. Le contrôle d’édition est traité comme un mot de passe. La valeur s’affiche à l’aide d’astérisques au lieu de faire écho aux caractères entrés.
    
DT_REQUIRED 
  
> Si le contrôle autorise les modifications (DT_EDITABLE), il doit avoir une valeur avant [l’appel d’IMAPIProp::SaveChanges](imapiprop-savechanges.md) . 
    
DT_SET_IMMEDIATE 
  
> Active le paramètre immédiat d’une valeur ; dès qu’une valeur du contrôle change, MAPI appelle la méthode **SetProps** pour la propriété associée à ce contrôle. Lorsque cet indicateur n’est pas défini, les valeurs sont définies lorsque la boîte de dialogue est ignorée. 
    
DT_SET_SELECTION 
  
> Lorsqu’une sélection est effectuée dans la zone de liste, la colonne d’index de cette zone de liste est définie en tant que propriété. Toujours utilisé avec DT_SET_IMMEDIATE.
    
Cette propriété est stockée dans le membre ulCtlFlags de la structure [DTCTL](dtctl.md) d’un contrôle. La plupart des indicateurs de contrôle s’appliquent à tous les contrôles qui autorisent l’entrée utilisateur ; quelques-uns s’appliquent uniquement au contrôle d’édition. Les contrôles qui n’autorisent pas l’entrée utilisateur, par exemple un bouton ou une étiquette, définissent 0 pour leurs indicateurs de contrôle. 
  
La plupart des valeurs d’indicateur sont explicites. Par exemple, lorsque DT_REQUIRED est défini pour un contrôle, il doit contenir une valeur avant que la boîte de dialogue ne soit autorisée à être ignorée. Soit le fournisseur de services peut fournir une valeur par le biais de son implémentation **IMAPIProp** , soit l’utilisateur peut en entrer une. DT_EDITABLE indique que la valeur du contrôle peut être modifiée. DT_MULTILINE permet à un contrôle d’édition de s’étendre sur plusieurs lignes. 
  
Certains indicateurs de contrôle ne sont pas si évidents dans leur signification. Lorsqu’un contrôle définit l’indicateur DT_SET_IMMEDIATE, les modifications apportées à sa valeur affectent dès que l’utilisateur passe à un nouveau contrôle. MAPI effectue un appel unique à la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de l’interface de propriété pour la propriété du contrôle. Ce comportement est différent du comportement par défaut, qui consiste à reporter l’effet des modifications apportées aux valeurs de contrôle jusqu’à ce que l’utilisateur sélectionne le bouton **OK** ou ferme la boîte de dialogue. L’indicateur DT_SET_IMMEDIATE est souvent utilisé en combinaison avec les notifications de table d’affichage. 
  
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
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

