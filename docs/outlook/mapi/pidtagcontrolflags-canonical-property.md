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
  
Contient un masque de réindicateur des indicateurs régissant le comportement d'un contrôle utilisé dans une boîte de dialogue construite à partir d'une table d'affichage.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTROL_FLAGS  <br/> |
|Identificateur :  <br/> |0x3F00  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Table d'affichage MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Un ou plusieurs des indicateurs suivants peuvent être définis pour cette propriété:
  
DT_ACCEPT_DBCS 
  
> Le contrôle peut contenir des caractères DBCS (Double-Byte Character Set). Cet indicateur est utilisé avec les contrôles d'édition. Il autorise des jeux de caractères codés sur plusieurs octets.
    
DT_EDITABLE 
  
> Le contrôle peut être modifié; la valeur associée au contrôle peut être modifiée. Lorsque cet indicateur n'est pas défini, le contrôle est en lecture seule. Cette valeur est ignorée sur l'étiquette, la zone de groupe, le bouton de commande standard, la zone de liste déroulante à valeurs multiples et les contrôles de zone de liste.
    
DT_MULTILINE 
  
> Le contrôle d'édition peut contenir plusieurs lignes. Cela signifie qu'un caractère de retour peut être entré dans le contrôle. Cet indicateur est valide uniquement pour les contrôles d'édition.
    
DT_PASSWORD_EDIT 
  
> S'applique aux contrôles d'édition. Le contrôle d'édition est traité comme un mot de passe. La valeur est affichée à l'aide d'astérisques au lieu de renvoyer les caractères réels entrés.
    
DT_REQUIRED 
  
> Si le contrôle autorise les modifications (DT_EDITABLE), il doit avoir une valeur avant [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) est appelé. 
    
DT_SET_IMMEDIATE 
  
> Active le paramétrage immédiat d'une valeur; dès qu'une valeur du contrôle est modifiée, MAPI appelle la méthode **SetProps** pour la propriété associée à ce contrôle. Lorsque cet indicateur n'est pas défini, les valeurs sont définies lorsque la boîte de dialogue est fermée. 
    
DT_SET_SELECTION 
  
> Lorsqu'une sélection est effectuée dans la zone de liste, la colonne d'index de cette zone de liste est définie en tant que propriété. Toujours utilisé avec DT_SET_IMMEDIATE.
    
Cette propriété est stockée dans le membre ulCtlFlags de la structure [DTCTL](dtctl.md) d'un contrôle. La plupart des indicateurs de contrôle s'appliquent à tous les contrôles qui autorisent l'entrée de l'utilisateur; quelques-unes s'appliquent uniquement au contrôle d'édition. Les contrôles qui n'autorisent pas l'entrée de l'utilisateur, tels qu'un bouton ou une étiquette, définissent 0 pour leurs indicateurs de contrôle. 
  
De nombreuses valeurs d'indicateur sont explicites. Par exemple, lorsque DT_REQUIRED est défini pour un contrôle, il doit contenir une valeur pour que la boîte de dialogue ne soit pas autorisée à être fermée. Le fournisseur de services peut fournir une valeur par le biais de son implémentation **IMAPIProp** ou l'utilisateur peut en entrer un. DT_EDITABLE indique que la valeur du contrôle peut être modifiée. DT_MULTILINE permet à la valeur d'un contrôle d'édition de s'étendre sur plusieurs lignes. 
  
Certains indicateurs de contrôle ne sont pas si évidents dans leur sens. Lorsqu'un contrôle définit l'indicateur DT_SET_IMMEDIATE, toutes les modifications apportées à sa valeur prennent effet dès que l'utilisateur passe à un nouveau contrôle. MAPI effectue un seul appel à la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) de l'interface de propriété pour la propriété du contrôle. Cela est différent du comportement par défaut, qui consiste à différer que les modifications apportées aux valeurs de contrôle prennent effet jusqu'à ce que l'utilisateur sélectionne le bouton **OK** ou ferme la boîte de dialogue. L'indicateur DT_SET_IMMEDIATE est souvent utilisé en combinaison avec des notifications de table d'affichage. 
  
Le tableau suivant répertorie les types de contrôles et toutes les valeurs d'indicateur pouvant être définies pour chaque type.
  
|**Control**|**Valeurs valides pour cette propriété**|
|:-----|:-----|
|Bouton  <br/> |Doit être égal à zéro  <br/> |
|Case à cocher  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Zone de liste modifiable  <br/> |DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Zone de liste déRoulante  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Edit  <br/> |DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Zone de groupe  <br/> |Doit être égal à zéro  <br/> |
|Étiquette  <br/> |Doit être égal à zéro  <br/> |
|Zone de liste  <br/> |Doit être égal à zéro  <br/> |
|Zone de liste déroulante à valeurs multiples  <br/> |Doit être égal à zéro  <br/> |
|Zone de liste à valeurs multiples  <br/> |Doit être égal à zéro  <br/> |
|Page à onglets  <br/> |Doit être égal à zéro  <br/> |
|Case d'option  <br/> |Doit être égal à zéro  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

