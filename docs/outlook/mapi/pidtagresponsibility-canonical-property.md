---
title: Propriété canonique PidTagResponsibility
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResponsibility
api_type:
- COM
ms.assetid: 1e8ccef1-db0a-4230-9bd0-87540b53e890
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 15bf61e71a2c230f7891c738661f839ecddb52e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330120"
---
# <a name="pidtagresponsibility-canonical-property"></a>Propriété canonique PidTagResponsibility

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur TRUE si un fournisseur de transport a déjà accepté la responsabilité de la remise du message à ce destinataire, et FALSe si le spouleur MAPI considère que ce fournisseur de transport doit accepter la responsabilité.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RESPONSIBILITY  <br/> |
|Identificateur :  <br/> |0x0E0F  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |MAPI non transmissible  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque le spouleur MAPI présente un message sortant à un fournisseur de transport, via [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md), il définit cette propriété sur false pour tous les destinataires pour lesquels le spouleur MAPI considère que le fournisseur de transport est responsable et true pour tous les autres destinataires. Le fournisseur de transport doit tenter de gérer tous les destinataires avec **PR_RESPONSIBILITY** défini sur false. Après l'envoi ou l'échec concluant de l'envoi à un destinataire, le fournisseur de transport doit définir cette propriété sur TRUE dans le message source pour indiquer qu'il a accepté la responsabilité pour ce destinataire. 
  
Si, après avoir examiné un destinataire, un fournisseur de transport décide qu'il ne peut pas ou ne doit pas le gérer, le fournisseur de transport doit laisser **PR_RESPONSIBILITY** défini sur false. Le spouleur MAPI recherche alors un autre fournisseur de transport pouvant gérer ce destinataire. Le spouleur MAPI crée finalement un rapport de non-remise pour les destinataires pour lesquels aucun fournisseur de transport n'accepte la responsabilité. 
  
Si le fournisseur de transport tente de remettre le message et ne le remet pas, il doit appeler la méthode [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) pour indiquer à MAPI les raisons de l'échec, afin que MAPI puisse générer un rapport de non-remise. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l'ordre et le flux de transfert de données entre un client et un serveur.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propri�t� canonique PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

