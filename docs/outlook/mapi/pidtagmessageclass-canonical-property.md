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
ms.openlocfilehash: d4e478b053bc1aa81643a60899480ac2ad9d4265
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786212"
---
# <a name="pidtagmessageclass-canonical-property"></a>Propriété canonique PidTagMessageClass

  
  
**S’applique à**: Outlook 
  
Contient une chaîne de texte qui identifie la classe de message défini par l’expéditeur, par exemple IPM. Note. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W  <br/> |
|Identificateur :  <br/> |0x001A du jeu  <br/> |
|Type de données :  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Zone :  <br/> |Common  <br/> |
   
## <a name="remarks"></a>Remarques

La classe de message indique le type du message. Il détermine l’ensemble des propriétés définies pour le message, le type d’informations le message dans le cas contraire et comment gérer le message. 
  
Ces propriétés contiennent des chaînes concaténées avec des périodes. Chaque chaîne représente un niveau de sous-classer. Par exemple, IPM. Remarque est une sous-classe de IPM et une superclasse de IPM. Note.Private. 
  
Ces propriétés doivent contenir des caractères ASCII 32 à 127 et ne doivent pas se terminer par un point (ASCII 46). Opérations de tri et de comparer doivent traiter comme une chaîne respectant la casse. La longueur maximale possible est de 255 caractères, mais afin de permettre à ajouter qualificateurs MAPI, il est recommandé que la longueur d’origine doivent être conservées sous 128 caractères. 
  
Chaque message est nécessaire pour fournir ces propriétés. En règle générale, l’application cliente création d’un nouveau message lui dès que [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) renvoyée avec succès. Mais si la propriété n’a pas été définie lorsque le client appelle [IMAPIProp::SaveChanges](imapiprop-savechanges.md), la banque de messages définissez-le IPM. 
  
Les valeurs définies par MAPI sont : 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

IPM et IPC sont destinés à être surclasse uniquement, et un message doit avoir au moins un qualificateur sous-classe ajouté avant d’être stockée ou envoyé. Pour plus d’informations sur l’utilisation des classes de message, consultez [Classes de Message](mapi-message-classes.md). Pour les listes de propriétés obligatoires et facultatifs pour les classes de message, consultez les sujets secondaires à propos des [Propriétés](message-properties-overview.md)de Message.
  
Une classe de message personnalisée peut définir des propriétés dans une plage réservée pour une utilisation avec cette classe de message uniquement. Pour plus d’informations, consultez la rubrique [Sur les identificateurs de propriété](mapi-property-identifier-overview.md). 
  
Contrôle de classes de message qui reçoivent un message entrant de dossier est stocké dans. Pour plus d’informations, voir la méthode [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . 
  
Pour plus d’informations sur l’utilisation des classes de messages avec des formulaires et des serveurs de formulaire, voir [choix d’une classe de Message](choosing-a-message-class.md). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.
    
[[MS-OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour la représentation des messages de messagerie et de télécopie de voix.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

