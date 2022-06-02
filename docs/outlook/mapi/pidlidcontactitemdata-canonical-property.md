---
title: Propriété canonique PidLidContactItemData
description: Décrit la propriété canonique PidLidContactItemData, qui est utilisée pour afficher les informations de contact.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidContactItemData
api_type:
- COM
ms.assetid: 411e8f81-c2b9-440a-9e9a-d6add5e4be63
ms.openlocfilehash: db367d98a7e562d5fe3e1b6dab8a151affed9ce8
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852655"
---
# <a name="pidlidcontactitemdata-canonical-property"></a>Propriété canonique PidLidContactItemData

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d’afficher les informations de contact.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidContactItemData  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID long (LID) :  <br/> |0x00008007  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Domaine :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

Si elle est présente, la propriété doit avoir six entrées, chacune correspondant à un champ visible dans l’interface utilisateur de l’application.
  
|**Index unique dans la propriété à valeurs multiples**|**La valeur doit être l’une des valeurs suivantes :**|**Description**|
|:-----|:-----|:-----|
|1  <br/> |0x00000001  <br/> |L’application doit afficher l’adresse d’accueil du contact. |
|1  <br/> |0x00000002 ou 0x00000000  <br/> |L’application doit afficher le travail du contact. |
|1  <br/> |0x00000003  <br/> |L’application doit afficher l’autre adresse du contact. |
|2  <br/> |0x00008080  <br/> |L’application doit afficher Email1. |
|2  <br/> |0x00008090  <br/> |L’application doit afficher Email2. |
|2  <br/> |0x000080A0  <br/> |L’application doit afficher Email3. |
|3,4,5,6  <br/> |PropertyID de l’une des propriétés téléphoniques ou des numéros de télécopie spécifiés dans [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx). |L’application doit afficher la propriété correspondante. |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées pour les contacts et les listes de distribution personnelles.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

