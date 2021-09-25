---
title: Propriété canonique PidTagResponsibility
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagResponsibility
api_type:
- COM
ms.assetid: 1e8ccef1-db0a-4230-9bd0-87540b53e890
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bae0e9ac805e0d95f70db164e517db1434c5431c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591506"
---
# <a name="pidtagresponsibility-canonical-property"></a>Propriété canonique PidTagResponsibility

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si un fournisseur de transport a déjà accepté la responsabilité de remettre le message à ce destinataire, et FALSE si lepooler MAPI considère que ce fournisseur de transport doit accepter la responsabilité.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RESPONSIBILITY  <br/> |
|Identificateur :  <br/> |0x0E0F  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |MAPI non transmetteable  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque lepooler MAPI présente un message sortant à un fournisseur de transport, via [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), il définit cette propriété sur FALSE pour tous les destinataires pour lesquels lepooler MAPI considère ce fournisseur de transport comme responsable, et TRUE pour tous les autres destinataires. Le fournisseur de transport doit tenter de gérer tous les destinataires dont **la PR_RESPONSIBILITY** définie sur FALSE. Après l’envoi réussi ou l’échec d’envoi à un destinataire, le fournisseur de transport doit définir cette propriété sur TRUE dans le message source pour indiquer qu’il a accepté la responsabilité de ce destinataire. 
  
Si, après avoir examiné un destinataire, un fournisseur de transport décide qu’il  ne peut pas ou ne doit pas le gérer, le fournisseur de transport doit laisser la PR_RESPONSIBILITY définie sur FALSE. Lepooler MAPI recherche ensuite un autre fournisseur de transport qui peut gérer ce destinataire. Lepooler MAPI crée finalement un rapport nondelivery pour tous les destinataires pour lesquels aucun fournisseur de transport n’accepte la responsabilité. 
  
Si le fournisseur de transport tente et ne parvient pas à remettre le message, il doit appeler la méthode [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) pour indiquer à MAPI les raisons de l’échec, afin que MAPI puisse générer un rapport non remis. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l’ordre et le flux des transferts de données entre un client et un serveur.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propri�t� canonique PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

