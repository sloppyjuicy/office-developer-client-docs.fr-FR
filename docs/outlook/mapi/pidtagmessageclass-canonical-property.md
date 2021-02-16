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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7912a3831333ff8a464a12e567430eb5a3272172
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359262"
---
# <a name="pidtagmessageclass-canonical-property"></a>Propriété canonique PidTagMessageClass

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une chaîne de caractères qui identifie la classe de message définie par l’expéditeur, telle qu’une note IPM. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W  <br/> |
|Identificateur :  <br/> |0x001A  <br/> |
|Type de données :  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Domaine :  <br/> |Courant  <br/> |
   
## <a name="remarks"></a>Remarques

La classe de message spécifie le type du message. Il détermine l’ensemble des propriétés définies pour le message, le type d’informations qu’il transmet et la façon de gérer le message. 
  
Ces propriétés contiennent des chaînes concatenées avec des périodes. Chaque chaîne représente un niveau de sous-classe. Par exemple, IPM. Notez qu’il s’agit d’une sous-classe d’IPM et d’une superclasse d’IPM. Note.Private. 
  
Ces propriétés doivent se composer des caractères ASCII 32 à 127 et ne doivent pas se terminer par un point (ASCII 46). Les opérations de tri et de comparaison doivent la traiter comme une chaîne qui ne respectera pas la cas. La longueur maximale possible est de 255 caractères, mais pour permettre à l’espace MAPI d’y appendre des qualificateurs, il est recommandé de conserver la longueur d’origine sous 128 caractères. 
  
Chaque message est requis pour fournir ces propriétés. Normalement, l’application cliente qui crée un message le définit dès que le message [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) est correctement envoyé. Toutefois, si la propriété n’a pas été définie lorsque le client appelle [IMAPIProp::SaveChanges,](imapiprop-savechanges.md)la magasin de messages doit la définir sur IPM. 
  
Les valeurs définies par MAPI sont : 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

Les IPM et IPC sont destinés à être des superclasses uniquement, et un message doit avoir au moins un qualificateur de sous-classe ajouté avant d’être stocké ou envoyé. Pour plus d’informations sur l’utilisation des classes de message, voir [Classes de message.](mapi-message-classes.md) Pour obtenir des listes de propriétés obligatoires et facultatives pour les classes de message, voir les sous-options de [About Message Properties](message-properties-overview.md).
  
Une classe de message personnalisée peut définir des propriétés dans une plage réservée à utiliser uniquement avec cette classe de message. Pour plus d’informations, voir [à propos des identificateurs de propriété.](mapi-property-identifier-overview.md) 
  
Les classes de message contrôlent le dossier de réception dans lequel un message entrant est stocké. Pour plus d’informations, voir la méthode [IMsgStore::GetReceiveFolderTable.](imsgstore-getreceivefoldertable.md) 
  
Pour plus d’informations sur l’utilisation de classes de message avec des formulaires et des serveurs de formulaires, voir [Choosing a Message Class](choosing-a-message-class.md). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server de protocole associées.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et pièce jointe.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les objets de message électronique.
    
[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées pour la représentation des messages vocaux et de télécopie.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

