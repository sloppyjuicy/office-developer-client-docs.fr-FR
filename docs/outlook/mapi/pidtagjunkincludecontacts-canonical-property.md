---
title: Propriété canonique PidTagJunkIncludeContacts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagJunkIncludeContacts
api_type:
- HeaderDef
ms.assetid: 25368f6c-4fba-4381-840c-ca122bd31b5f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: df31fbcfd5f238c99e4b5a82771cea1bccf0403f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595230"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a>Propriété canonique PidTagJunkIncludeContacts

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique si les adresses e-mail des contacts dans le dossier Contacts sont traitées spécialement en ce qui concerne le filtre de courrier indésirable.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_JUNK_INCLUDE_CONTACTS  <br/> |
|Identificateur :  <br/> |0x6100  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Courrier indésirable  <br/> |
   
## <a name="remarks"></a>Remarques

Si la propriété est définie sur « 0x00000001 », ces adresses de messagerie doivent remplir la partie « approuvé » de la restriction de règle de courrier indésirable afin que le courrier provenant de ces adresses soit considéré comme « non indésirable ». Si la valeur est « 0x00000000 », les adresses de messagerie du dossier Contacts ne doivent pas être ajoutées à la règle de courrier indésirable et la section de la règle doit être NULL.
  
Si cette propriété est présente avec la valeur « 0x00000001 » et si le contact ajouté a des adresses de messagerie qui ne sont pas encore incluses dans la section contacts de confiance de la règle de courrier indésirable, ces adresses de messagerie doivent être ajoutées à la restriction. Si cette propriété est « 0x00000000 », aucune action n’est requise.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permet la gestion des listes d’adresses de courriers électroniques indésirables et la détermination des listes d’adresses de courrier indésirable.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

