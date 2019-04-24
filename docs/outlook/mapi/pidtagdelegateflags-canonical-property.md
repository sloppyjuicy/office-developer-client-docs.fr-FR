---
title: Propriété canonique PidTagDelegateFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDelegateFlags
api_type:
- HeaderDef
ms.assetid: 3a504594-204c-472c-8be7-dca154c94ea2
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 20ffc6f7f4d21f980e5f0f387464430ba187192a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359898"
---
# <a name="pidtagdelegateflags-canonical-property"></a>Propriété canonique PidTagDelegateFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique si un délégué peut afficher les objets de message privés de la personne ayant la délégation.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DELEGATE_FLAGS  <br/> |
|Identificateur :  <br/> |0x686B  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Domaine :  <br/> |Transmission définie par la classe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Chaque entrée de cette propriété doit être définie sur l'une des valeurs suivantes.
  
|**Indicateur**|**Value**|**Description**|
|:-----|:-----|:-----|
|HidePrivate  <br/> |0  <br/> |Le délégué ne doit pas être autorisé à afficher des objets de message privés.  <br/> |
|ShowPrivate  <br/> |0,1  <br/> |Le délégué doit être autorisé à afficher des objets de message privés.  <br/> |
   
Cette propriété doit être définie dans l'objet information de délégué. La valeur de «ShowPrivate» indique que la personne qui a besoin de créer des objets de message privés est visible. Cette préférence s'applique à tous les dossiers pour lesquels le délégué a le rôle de réviseur, d'auteur ou d'éditeur.
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Spécifie les méthodes de connexion et de configuration des boîtes aux lettres en tant que délégués, ainsi que les interactions avec les objets message et Calendar lorsqu'ils agissent pour le compte d'un autre utilisateur.
    
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

