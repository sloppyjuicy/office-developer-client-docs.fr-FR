---
title: Encodage d’un message avec TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: cdaa03cfbc0bbd0fcf6a320ecf8fae9f372d5781
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336700"
---
# <a name="encoding-a-message-with-tnef"></a>Encodage d’un message avec TNEF

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lors de l'envoi d'un message, le fournisseur de transport peut créer un fichier utilisé pour contenir le message pendant la transmission. Ensuite, une interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) est encapsulée autour du fichier. Le fournisseur de transport utilise ensuite les méthodes [ITnef](itnefiunknown.md) pour écrire les propriétés de message dans le flux dans un format balisé qui permet de facilement décoder les propriétés par les fournisseurs de transport de réception. 
  
**Pour représenter un message entier dans un seul fichier**
  
1. Obtenir un objet TNEF en transmettant un objet [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) et un message dans la fonction [OpenTnefStreamEx](opentnefstreamex.md) . 
    
2. Obtenir la liste de toutes les propriétés définies pour le message en appelant la méthode [IMAPIProp:: GetPropList](imapiprop-getproplist.md) . 
    
3. Utilisez les méthodes [IMAPIProp](imapipropiunknown.md) pour exclure toutes les propriétés prises en charge par le système de messagerie. À un moment approprié, écrivez ces propriétés dans le système de messagerie au format requis par le système de messagerie. 
    
4. Appelez [ITnef:: AddProps](itnef-addprops.md) pour coder les autres propriétés, y compris toutes les pièces jointes. 
    
5. Appelez la méthode [ITnef:: Finish](itnef-finish.md) pour coder le message dans le flux TNEF une fois toutes les propriétés demandées ajoutées. 
    
6. Appelez la méthode [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) pour obtenir le texte du message balisé. Ce texte balisé est écrit dans le système de messagerie à l'aide de méthodes de l'interface OLE [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) . 
    
7. Appelez la méthode [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) pour libérer l'objet **ITnef** . 
    
**Pour traiter un message TNEF entrant**
  
1. Obtenir un objet de message MAPI à partir du spouleur MAPI et écrire les propriétés d'en-tête de message dans le nouveau message MAPI.
    
2. Créer et initialiser un objet [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) pour contenir les données TNEF à partir du message entrant. 
    
3. TransMettez le message MAPI et l'objet [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) à la fonction [OpenTnefStreamEx](opentnefstreamex.md) . 
    
4. Décodez les informations contenues dans les données TNEF en appelant la méthode [ITnef:: ExtractProps](itnef-extractprops.md) . 
    
   > [!NOTE]
   > Tout ce qui est décodé par **ExtractProps** remplace les propriétés décodées de l'enveloppe du message entrant. Autrement dit, les propriétés TNEF extraites remplacent les propriétés existantes dans un message. 
  
5. Traitez le texte du message balisé en appelant [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) et analysez le texte afin de récupérer les positions des pièces jointes. 
    
6. Enregistrez le message en appelant [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).
    
7. Libérez l'objet TNEF en appelant la méthode [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) . 
    

