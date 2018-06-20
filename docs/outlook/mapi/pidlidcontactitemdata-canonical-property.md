---
title: Propriété canonique PidLidContactItemData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactItemData
api_type:
- COM
ms.assetid: 411e8f81-c2b9-440a-9e9a-d6add5e4be63
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 510920af290fa1cfe13fc1a85ba72f902532c539
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785105"
---
# <a name="pidlidcontactitemdata-canonical-property"></a>Propriété canonique PidLidContactItemData

  
  
**S’applique à**: Outlook 
  
Permet d’afficher les informations de contact.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidContactItemData  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID de type long (capot) :  <br/> |0x00008007  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Zone :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

S’il est présent, la propriété doit avoir six entrées, chacun correspondant à un champ visible dans l’interface utilisateur de l’application.
  
|**Index de base 1 dans la propriété à valeurs multiples**|**La valeur doit être une des options suivantes**|**Description**|
|:-----|:-----|:-----|
|1  <br/> |0x00000001  <br/> |L’application doit afficher l’adresse du contact personnel.  <br/> |
|1  <br/> |0 x 00000002 ou 0 x 00000000  <br/> |L’application doit afficher le travail du contact.  <br/> |
|1  <br/> |0 x 00000003  <br/> |L’application doit afficher le contact de l’autre adresse.  <br/> |
|2  <br/> |0x00008080  <br/> |L’application doit afficher les messages électroniques 1.  <br/> |
|2  <br/> |0x00008090  <br/> |L’application doit afficher 2.  <br/> |
|2  <br/> |0x000080A0  <br/> |L’application doit afficher messagerie3.  <br/> |
|3,4,5,6  <br/> |PropertyID de toutes les propriétés de téléphone ou l’un des numéros de télécopie sont spécifiés dans [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).  <br/> |L’application doit afficher la propriété correspondante.  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

