---
title: Traitement TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d324fb3-d917-4502-b3a4-179c479deb79
description: 'Derni�re modification�: jeudi 5 juillet 2012'
ms.openlocfilehash: 066ad3dfb64161e326b92fef7774d5b3b9461d8a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339598"
---
# <a name="tnef-processing"></a>Traitement TNEF

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La série d'actions suivante décrit la façon dont les transports utilisent les méthodes TNEF pour traiter les messages sortants et entrants.
  
 **Pour envoyer un message incluant un flux TNEF**
  
1. Traitez les propriétés de message prises en charge par le système de messagerie.
    
2. Marquer le message de manière spécifique à une implémentation de sorte que le fournisseur de transport de réception puisse déterminer que le message nécessite un traitement TNEF. Par exemple, un fournisseur de transport TNEF qui envoie des messages vers un système de messagerie SMTP peut ajouter un champ d'en-tête personnalisé tel que «X-CONTAINs-TNEF» pour indiquer que le message contient des données TNEF.
    
3. Obtenez un objet TNEF et utilisez-le pour encapsuler les propriétés de message qui ne sont pas prises en charge par le système de messagerie dans un flux TNEF.
    
4. Codez le flux TNEF à l'aide du modèle de pièces jointes du système de messagerie. Par exemple, si le modèle de pièce jointe sous-jacente concerne les pièces jointes uuencode et les ajoute au texte du message, le fournisseur de transport doit alors uuencode le flux TNEF en une autre pièce jointe. Le fournisseur de transport doit également implémenter une méthode pour identifier quelle pièce jointe contient le flux TNEF encodé lors de la réception d'un message. La méthode standard pour marquer cette pièce jointe est de lui attribuer un nom de fichier de pièce jointe «WINMAIL. DAT». Si c'est le cas de votre fournisseur de transport, tous les autres fournisseurs de transport compatibles TNEF qui suivent cette Convention pourront interagir avec.
    
5. Utilisez [ITnef:](itnefiunknown.md) méthodes d'interface IUnknown pour insérer des balises décrivant les positions des pièces jointes des messages dans le texte du message. 
    
6. Accédez au texte du message balisé via les méthodes [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) , puis envoyez-le au système de messagerie. 
    
 **Pour récupérer des propriétés encapsulées**
  
1. Écrivez les propriétés prises en charge par le système de messagerie dans un nouveau message, y compris le texte du message balisé qui contient les propriétés encapsulées.
    
2. Décodez le flux TNEF à partir de la pièce jointe appropriée.
    
3. Décodez toutes les autres pièces jointes et écrivez-les dans de nouvelles pièces jointes MAPI sur un message.
    
4. Ouvrez le flux TNEF pour le décodage à l'aide de la fonction [OpenTnefStreamEx](opentnefstreamex.md) . 
    
5. Utilisez la méthode [ITnef:: ExtractProps](itnef-extractprops.md) pour décoder le flux TNEF et écrire les propriétés encapsulées dans le nouveau message. Toutes les propriétés codées qui sont des doublons de propriétés non codées remplacent les propriétés non codées lorsque les propriétés codées sont décodées. 
    
6. Utilisez la méthode [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) pour analyser le texte du message afin de récupérer les positions des pièces jointes à partir des balises du texte du message. 
    

