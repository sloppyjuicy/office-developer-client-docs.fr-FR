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
ms.openlocfilehash: 031e5483539ce17c8b9b994690985c2349573e27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319508"
---
# <a name="pidlidcontactitemdata-canonical-property"></a>Propriété canonique PidLidContactItemData

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d'afficher les informations de contact.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidContactItemData  <br/> |
|Jeu de propriétés:  <br/> |PSETID_Address  <br/> |
|ID long (couvercle):  <br/> |0x00008007  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Domaine :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

S'il est présent, la propriété doit avoir six entrées, chacune correspondant à un champ visible dans l'interface utilisateur de l'application.
  
|**Index de base 1 dans la propriété à valeurs multiples**|**La valeur doit être l'une des valeurs suivantes:**|**Description**|
|:-----|:-----|:-----|
|0,1  <br/> |0x00000001  <br/> |L'application doit afficher l'adresse d'accueil du contact.  <br/> |
|0,1  <br/> |0x00000002 ou 0x00000000  <br/> |L'application doit afficher le travail du contact.  <br/> |
|0,1  <br/> |0x00000003  <br/> |L'application doit afficher l'autre adresse du contact.  <br/> |
|n°2  <br/> |0x00008080  <br/> |L'application doit afficher Email1.  <br/> |
|n°2  <br/> |0x00008090  <br/> |L'application doit afficher Email2.  <br/> |
|n°2  <br/> |0x000080A0  <br/> |L'application doit afficher Email3.  <br/> |
|3, 4, 5, 6  <br/> |PropertyID de toutes les propriétés téléphoniques ou des numéros de télécopie spécifiés dans [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).  <br/> |L'application doit afficher la propriété correspondante.  <br/> |
   
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelle.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

