---
title: Propriété canonique PidTagContactAddressBookFolderName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContactAddressBookFolderName
api_type:
- HeaderDef
ms.assetid: 6149da2f-6e42-429c-bcdb-d517d21df720
description: Contient un nom de dossier utilisé pour les entrées de carnet d’adresses Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: d3dc2b914052dd67d40f0629ed6e6bce42c806f9
ms.sourcegitcommit: c68b7b7f98b3ff9e6de37ee5877adcad2e5e71d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63741671"
---
# <a name="pidtagcontactaddressbookfoldername-canonical-property"></a>Propriété canonique PidTagContactAddressBookFolderName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un nom de dossier utilisé pour les entrées de carnet d’adresses.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTAB_FOLDER_NAME, PR_CONTAB_FOLDER_NAME_W  <br/> |
|Identificateur :  <br/> |0x6613  <br/> |
|Type de données :  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Domaine :  <br/> |Carnet d’adresses de contact  <br/> |
   
## <a name="remarks"></a>Remarques

Les caractères suivants ne peuvent pas être utilisés dans les noms de dossiers :
  
[ ] / \ &amp; ~ ? \* | \< \> " ; : +
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

