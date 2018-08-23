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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d2a1c49b29ba08775768fc74861ba36b3c6356fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589377"
---
# <a name="pidtagresponsibility-canonical-property"></a>Propriété canonique PidTagResponsibility

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient la valeur TRUE si un fournisseur de transport a déjà accepté responsable de la remise du message à ce destinataire et FALSE si le spouleur MAPI estime que ce fournisseur de transport doit accepter la responsabilité.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RESPONSIBILITY  <br/> |
|Identificateur :  <br/> |0x0E0F  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |MAPI non transmissible  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque le spouleur MAPI présente un message sortant à un fournisseur de transport, par le biais [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), elle définit cette propriété sur FALSE pour tous les destinataires pour lesquels le spouleur MAPI considère ce fournisseur de transport chargé et la valeur TRUE pour tous les autres destinataires. Le fournisseur de transport doit essayer de gérer tous les destinataires avec **PR_RESPONSIBILITY** définie sur FALSE. Après avoir correctement l’envoi ou ait cessé d’envoyer, à un destinataire, le fournisseur de transport doit définir cette propriété sur TRUE dans le message source pour indiquer qu’il a accepté la responsabilité du destinataire. 
  
Si, après avoir examiné un destinataire, un fournisseur de transport décide qu’il ne peut pas ou qu’il ne doit pas gérer, le fournisseur de transport doit conserver la valeur **PR_RESPONSIBILITY** sur FALSE. Le spouleur MAPI recherchera ensuite un autre fournisseur de transport qui peut gérer ce destinataire. Finalement, le spouleur MAPI crée un rapport de non-remise pour tous les destinataires pour lesquels aucun fournisseur de transport n’accepte la responsabilité. 
  
Si le fournisseur de transport tente et ne parvient pas à remettre le message, il doit appeler la méthode [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) pour indiquer à MAPI les raisons de l’échec, afin que MAPI peut générer un rapport de non-remise. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propri�t� canonique PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

