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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8590e357252089aaa49a71d443037b9b9ed77ee4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356741"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a>Propriété canonique PidTagReceiveFolderSettings

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau des paramètres de dossier de réception d'une banque de messages.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECEIVE_FOLDER_SETTINGS  <br/> |
|Identificateur :  <br/> |0x3415  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Domaine :  <br/> |Banque de messages MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut être exclue dans [IMAPIProp:: CopyTo](imapiprop-copyto.md) Operations ou incluse dans [IMAPIProp:: CopyProps](imapiprop-copyprops.md) Operations. En tant que propriété de type PT_OBJECT, elle ne peut pas être récupérée avec succès par la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) ; son contenu doit être accessible à l'aide de la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , qui demande l'interface avec l'identificateur IID_IMAPITable. Les fournisseurs de services doivent le signaler à la méthode [IMAPIProp:: GetPropList](imapiprop-getproplist.md) s'il est défini, mais peuvent éventuellement le signaler ou non s'il n'est pas défini. 
  
Pour récupérer le contenu de la table, une application cliente doit appeler la méthode [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . Pour plus d'informations, consultez la rubrique [Receive Folder tables](receive-folder-tables.md).
  
Cette propriété contient un tableau des mappages des dossiers de réception pour la Banque de messages. L'appel de **OpenProperty** sur cette propriété équivaut à l'appel de **GetReceiveFolderTable** sur la Banque de messages. 
  
## <a name="related-resources"></a>Ressources associées

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

