---
title: Propriété canonique PidTagJunkAddRecipientsToSafeSendersList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkAddRecipientsToSafeSendersList
api_type:
- HeaderDef
ms.assetid: 78543caa-e6ec-4ac7-bfdd-70c56f8fd955
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8c104af106a885f42f8063bcf5fb55d654f2688e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786153"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a>Propriété canonique PidTagJunkAddRecipientsToSafeSendersList

  
  
**S’applique à**: Outlook 
  
Indique si les destinataires de messagerie à ajouter à la liste des expéditeurs approuvés.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_JUNK_ADD_RECIPS_TO_SSL  <br/> |
|Identificateur :  <br/> |0x6103  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Courrier indésirable  <br/> |
   
## <a name="remarks"></a>Remarques

Le cas échéant, cette propriété doit être définie sur 0 ou 1. Une valeur de 1 indique que les destinataires de messagerie sont à ajouter à la liste des expéditeurs approuvés. Une valeur de 0 indique que les destinataires de messagerie ne doivent ne pas figurer dans la liste des expéditeurs approuvés.
  
Si cette propriété est présente avec la valeur 1, les adresses SMTP des destinataires de courrier électronique doivent être ajoutés à la clause d’expéditeurs approuvés de la condition de règle de courrier indésirable. Si cette propriété est 0, aucune action n’est requise.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permet la gestion des listes autoriser/bloquer et la détermination des messages de courrier indésirable.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

