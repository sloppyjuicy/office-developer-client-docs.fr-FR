---
title: Propriété canonique PidTagMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageClass
api_type:
- HeaderDef
ms.assetid: 1e704023-1992-4b43-857e-0a7da7bc8e87
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7912a3831333ff8a464a12e567430eb5a3272172
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359262"
---
# <a name="pidtagmessageclass-canonical-property"></a>Propriété canonique PidTagMessageClass

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une chaîne de texte qui identifie la classe de message définie par l'expéditeur, telle que IPM. Note. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W  <br/> |
|Identificateur :  <br/> |0x001A  <br/> |
|Type de données :  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Domaine :  <br/> |Courant  <br/> |
   
## <a name="remarks"></a>Remarques

La classe de message spécifie le type du message. Il détermine le jeu de propriétés défini pour le message, le type d'informations que le message achemine et la façon de gérer le message. 
  
Ces propriétés contiennent des chaînes concaténées avec des points. Chaque chaîne représente un niveau de sous-Class. Par exemple, IPM. Note est une sous-classe de IPM et une superclasse de IPM. Note. private. 
  
Ces propriétés doivent être constituées des caractères ASCII 32 à 127 et ne doivent pas se terminer par un point (ASCII 46). Les opérations de tri et de comparaison doivent les traiter comme une chaîne ne respectant pas la casse. La longueur maximale possible est de 255 caractères, mais pour permettre à la salle MAPI d'ajouter des qualificateurs, il est recommandé de conserver la longueur d'origine sous 128 caractères. 
  
Chaque message est requis pour fournir ces propriétés. Normalement, l'application cliente qui crée un nouveau message le définit dès que [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) renvoie avec succès. Toutefois, si la propriété n'a pas été définie lorsque le client appelle [IMAPIProp:: SaveChanges](imapiprop-savechanges.md), la Banque de messages doit la définir sur IPM. 
  
Les valeurs définies par MAPI sont les suivantes: 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

IPM et IPC sont destinés à être des superclasses uniquement, et un message doit avoir au moins un qualificateur de sous-classe ajouté avant d'être stocké ou envoyé. Pour plus d'informations sur l'utilisation de la classe de message, consultez la rubrique [classes de message](mapi-message-classes.md). Pour obtenir la liste des propriétés requises et facultatives pour les classes de message, reportez-vous aux sous-rubriques de la rubrique [about message Properties](message-properties-overview.md).
  
Une classe de message personnalisée peut définir les propriétés d'une plage réservée à utiliser avec cette classe de message uniquement. Pour plus d'informations, consultez la rubrique [à propos](mapi-property-identifier-overview.md)des identificateurs de propriétés. 
  
Les classes de message contrôlent le dossier de réception dans lequel un message entrant est stocké. Pour plus d'informations, reportez-vous à la méthode [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . 
  
Pour plus d'informations sur l'utilisation de classes de message avec des serveurs de formulaires et de formulaires, voir [Choosing a message Class](choosing-a-message-class.md). 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et Attachment.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.
    
[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées pour la représentation des messages vocaux et de télécopie.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés indiquées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

