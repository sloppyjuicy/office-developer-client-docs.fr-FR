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
ms.openlocfilehash: 56f6e2355ee2e64cc766bafe27cd59454e210ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315420"
---
# <a name="pidlidusetnef-canonical-property"></a>Propriété canonique PidLidUseTnef

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique si le format TNEF (Transport Neutral Encapsulation Format) doit être inclus dans un message lors de la conversion de MAPI en format MIME (Multipurpose Internet Mail Extensions) ou SMTP (Simple Mail Transfer Protocol).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidUseTNEF  <br/> |
|Jeu de propriétés:  <br/> |PSETID_Common  <br/> |
|ID long (couvercle):  <br/> |0x00008582  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Configuration de l'exécution  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété spécifie si TNEF doit être inclus dans un message lors de la conversion du format TNEF au format MIME ou SMTP. Cette propriété peut être absente et, si tel est le cas, TNEF ne doit pas être inclus dans le message.
  
Cette propriété s'applique uniquement lorsque le message est envoyé à partir d'un compte de messagerie POP3/SMTP et ne s'applique pas lorsque le message est envoyé par d'autres fournisseurs, tels que Microsoft Exchange Server.
  
Dans certaines circonstances, par exemple lorsque les boutons de vote sont activés ou qu'un objet incorporé OLE est attaché à un message, Outlook peut définir cette propriété afin de forcer l'utilisation de TNEF.
  
La propriété **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) peut être utilisée pour appliquer uniquement du texte brut, et non au format TNEF, lors de l'envoi d'un message. Étant donné que **PidLidUseTNEF** remplace le paramètre dans **PR_MSG_EDITOR_FORMAT**, une application qui souhaite forcer le texte brut sur un message sortant doit également rechercher **PIDLIDUSETNEF** et la réinitialiser sur false. En outre, le complément doit supprimer les fonctionnalités de message qui nécessitaient le format TNEF pour éviter que les pièces jointes inutilisables du message soient finalement envoyées. 
  
Utilisez l'indicateur **CCSF_USE_TNEF** lors de l'appel de [IConverterSession:: MAPItoMIMEStm](iconvertersession-mapitomimestm.md) pour convertir un message MAPI sortant en flux MIME peut également appliquer le format TNEF. Cela s'applique même si **PidLidUseTNEF** n'est pas défini. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Encode et décode les objets message et Attachment en une représentation de flux efficace.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

