---
title: Propriété canonique PidLidUseTnef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidUseTnef
api_type:
- COM
ms.assetid: 954048d6-e2eb-43e7-b52c-c2f047bb84a4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d5d38f98402c0804633d3bcb0f9ca196fa15795f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610054"
---
# <a name="pidlidusetnef-canonical-property"></a>Propriété canonique PidLidUseTnef

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie si le format TNEF (Transport Neutral Encapsulation Format) doit être inclus dans un message lorsque ce message est converti du format MAPI au format MIME (Multipurpose Internet Mail Extensions) ou SMTP (Simple Mail Transfer Protocol).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidUseTNEF  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x00008582  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Configuration au moment de l’exécuter  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété spécifie si le format TNEF doit être inclus dans un message lorsque ce message est converti du format TNEF au format MIME ou SMTP. Cette propriété peut être absente et, si tel est le cas, le TNEF ne doit pas être inclus dans le message.
  
Cette propriété s’applique uniquement lorsque le message est envoyé à partir d’un compte de messagerie POP3/SMTP et ne s’applique pas lorsque le message est envoyé par d’autres fournisseurs, tels que Microsoft Exchange Server.
  
Dans certaines circonstances, par exemple lorsque les boutons de vote sont activés ou qu’un objet OLE incorporé est joint à un message, Outlook peut définir cette propriété pour forcer l’utilisation du TNEF.
  
La **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) peut être utilisée pour appliquer uniquement le texte simple, et non le TNEF, lors de l’envoi d’un message. Étant donné que **PidLidUseTNEF** remplace le paramètre dans **PR_MSG_EDITOR_FORMAT**, une application qui souhaite forcer le texte simple sur un message sortant doit également rechercher **PidLidUseTNEF** et le redéfinir sur FALSE. En outre, le complément doit supprimer les fonctionnalités de message qui nécessitaient le TNEF pour éviter les pièces jointes inutilisables sur le message qui est finalement envoyé. 
  
Utilisez **l’indicateur CCSF_USE_TNEF** lors de l’appel de [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) pour convertir un message MAPI sortant en flux MIME peut également appliquer le TNEF. Cela s’applique même **si PidLidUseTNEF n’est** pas définie. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les objets de message électronique.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Encode et décode les objets de message et de pièce jointe dans une représentation de flux efficace.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

