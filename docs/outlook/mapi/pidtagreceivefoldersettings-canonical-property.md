---
title: Propriété canonique PidTagReceiveFolderSettings
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagReceiveFolderSettings
api_type:
- COM
ms.assetid: 2f0b1679-05b0-4580-b6d2-474fe3f9d012
description: Contient une table des paramètres de dossier de réception d’une boutique de messages. Son contenu doit être accessible par la méthode IMAPIProp::OpenProperty.
ms.openlocfilehash: 2ae334b47fdc761fd6a842ebf4d0d78fb0a84412
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63764635"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a>Propriété canonique PidTagReceiveFolderSettings

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une table des paramètres de dossier de réception d’une boutique de messages.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECEIVE_FOLDER_SETTINGS  <br/> |
|Identificateur :  <br/> |0x3415  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Domaine :  <br/> |Magasin de messages MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut être exclue dans les opérations [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluse dans les opérations [IMAPIProp::CopyProps](imapiprop-copyprops.md) . En tant que propriété de type PT_OBJECT, elle ne peut pas être récupérée avec succès par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) ; Son contenu doit être accessible par la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , demandant l’interface avec l’identificateur IID_IMAPITable. Les fournisseurs de services doivent le signaler à la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) si elle est définie, mais peuvent éventuellement la signaler ou non si elle n’est pas définie. 
  
Pour récupérer le contenu de la table, une application cliente doit appeler la méthode [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . Pour plus d’informations, voir [Tables des dossiers de réception](receive-folder-tables.md).
  
Cette propriété contient une table des mappages des dossiers de réception pour la magasin de messages. Appeler **OpenProperty sur** cette propriété équivaut à appeler **GetReceiveFolderTable** sur la boutique de messages. 
  
## <a name="related-resources"></a>Ressources connexes

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

