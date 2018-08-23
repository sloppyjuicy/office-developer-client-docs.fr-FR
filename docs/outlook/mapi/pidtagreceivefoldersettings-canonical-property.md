---
title: Propriété canonique PidTagReceiveFolderSettings
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceiveFolderSettings
api_type:
- COM
ms.assetid: 2f0b1679-05b0-4580-b6d2-474fe3f9d012
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c8bd8c7fb2ff5a030cd96e4c3ac2bbb4b6b16ce5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571457"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a>Propriété canonique PidTagReceiveFolderSettings

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un tableau d’un message de la banque de recevoir des paramètres du dossier.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECEIVE_FOLDER_SETTINGS  <br/> |
|Identificateur :  <br/> |0x3415  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Domaine :  <br/> |Banque de messages MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut être exclue dans les opérations [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluse dans les opérations de [IMAPIProp::CopyProps](imapiprop-copyprops.md) . En tant que propriété de type PT_OBJECT, il ne peut pas être récupéré par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) ; son contenu doit être accessible par la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , qui demande à l’interface avec l’identificateur IID_IMAPITable. Fournisseurs de services doivent signaler à la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) s’il est défini, mais peut le signaler ou pas si elle n’est pas définie. 
  
Pour récupérer le contenu du tableau, une application cliente doit appeler la méthode [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . Pour plus d’informations, voir [S’afficher les Tables de dossier](receive-folder-tables.md).
  
Cette propriété contient une table de mappages de dossiers receive pour la banque de messages. L’appel **OpenProperty** sur cette propriété est équivalente à l’appel **GetReceiveFolderTable** sur la banque de messages. 
  
## <a name="related-resources"></a>Ressources connexes

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

