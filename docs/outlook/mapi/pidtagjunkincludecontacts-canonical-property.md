---
title: Propriété canonique PidTagJunkIncludeContacts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkIncludeContacts
api_type:
- HeaderDef
ms.assetid: 25368f6c-4fba-4381-840c-ca122bd31b5f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4dde93bbec2594804ab18a3ee4eb3e116a57e528
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786160"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a>Propriété canonique PidTagJunkIncludeContacts

  
  
**S’applique à**: Outlook 
  
Indique si les adresses de messagerie des contacts du dossier Contacts sont traités spécialement en ce qui concerne le filtre de courrier indésirable.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_JUNK_INCLUDE_CONTACTS  <br/> |
|Identificateur :  <br/> |0x6100  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Courrier indésirable  <br/> |
   
## <a name="remarks"></a>Remarques

Si la valeur « 0 x 00000001 », ces adresses de messagerie doivent remplir la partie de la Restriction de règle de courrier indésirable adresse de messagerie du contact « approuvés » tels que le courrier provenant de ces adresses est considéré comme « pas de courrier indésirable ». Si la valeur « 0 x 00000000 », les adresses de messagerie à partir du dossier Contacts ne doivent pas être ajoutés à la règle de courrier indésirable et la section de la règle doit être NULL.
  
Si cette propriété est présente avec la valeur « 0 x 00000001 » et si le contact ajouté les adresses de messagerie qui ne sont pas encore inclus dans la section contacts approuvé de la règle de courrier indésirable, les adresses de messagerie doivent être ajoutés à la restriction. Si cette propriété est « 0 x 00000000 », aucune action n’est requise.
  
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

