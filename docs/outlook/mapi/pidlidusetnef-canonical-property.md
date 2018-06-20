---
title: Propriété canonique PidLidUseTnef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidUseTnef
api_type:
- COM
ms.assetid: 954048d6-e2eb-43e7-b52c-c2f047bb84a4
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 73fa4311a61be9259d8c45aca79d719785c213a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785529"
---
# <a name="pidlidusetnef-canonical-property"></a>Propriété canonique PidLidUseTnef

  
  
**S’applique à**: Outlook 
  
Spécifie si le Transport Neutral Encapsulation Format (TNEF) doivent être inclus dans un message lorsque ce message est converti en message MAPI au format Multipurpose Internet Mail Extensions (MIME) ou SMTP Simple Mail Transfer Protocol ().
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidUseTNEF  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID de type long (capot) :  <br/> |0x00008582  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Zone :  <br/> |Configuration d’exécution  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété spécifie si le format TNEF doit être inclus dans un message lorsque ce message est converti en message TNEF au format MIME ou SMTP. Cette propriété peut être absente et si Oui, TNEF ne doit pas être incluse dans le message.
  
Cette propriété s’applique uniquement lorsque le message est envoyé à partir d’un compte de messagerie POP3/SMTP et ne s’applique pas lorsque le message est envoyé par d’autres fournisseurs, tels que Microsoft Exchange Server.
  
Dans certaines circonstances, telles que lors de vote sont activées ou incorporé OLE object est joint à un message, Outlook peut définir cette propriété pour forcer l’utilisation du format TNEF.
  
La propriété **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) peut être utilisée pour appliquer uniquement du texte brut et pas TNEF, lors de l’envoi d’un message. Comme **PidLidUseTNEF** remplace le paramètre de **PR_MSG_EDITOR_FORMAT**, une application pour forcer le texte brut d’un message sortant doit également rechercher **PidLidUseTNEF** et rétablir à FALSE. En outre, le complément doit supprimer les fonctionnalités de message TNEF éviter les pièces jointes inutilisables dans le message est envoyé pour finir de requis. 
  
Utiliser l’indicateur **CCSF_USE_TNEF** lors de l’appel [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) pour convertir un message MAPI sortant à un flux MIME peut également appliquer TNEF. Cela s’applique même si **PidLidUseTNEF** n’est pas défini. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

