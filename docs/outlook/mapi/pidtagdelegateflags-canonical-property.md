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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d43ec0bd2978c64e3a5ceb635f0dcda57de01cfd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590735"
---
# <a name="pidtagdelegateflags-canonical-property"></a>Propriété canonique PidTagDelegateFlags

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Spécifie si un délégué peut afficher des objets de message privé de la personne.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DELEGATE_FLAGS  <br/> |
|Identificateur :  <br/> |0x686B  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Domaine :  <br/> |Message défini par la classe transmissible  <br/> |
   
## <a name="remarks"></a>Remarques

Chaque entrée de cette propriété doit être définie sur une des valeurs suivantes.
  
|**Flag**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|HidePrivate  <br/> |0  <br/> |Le délégué doit pas afficher les objets de message privé.  <br/> |
|ShowPrivate  <br/> |1  <br/> |Le délégué convient pour afficher les objets de message privé.  <br/> |
   
Cette propriété doit être définie dans l’objet d’informations de délégué. La valeur de « ShowPrivate » indique que la personne souhaite afficher les objets de message privé. Cette préférence s’applique à tous les dossiers pour lesquels le délégué a un rôle réviseur, auteur ou l’éditeur.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les objets de messagerie et de calendrier lorsqu’ils agissent au nom d’un autre utilisateur.
    
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

