---
title: Traitement TNEF
description: Décrit le traitement TNEF et décrit comment les transports utilisent les méthodes TNEF pour traiter les messages sortants et entrants.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4d324fb3-d917-4502-b3a4-179c479deb79
ms.openlocfilehash: bbaadd083093dbe3c76f07138b0b51e56e205a31
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894788"
---
# <a name="tnef-processing"></a>Traitement TNEF

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La série d’actions suivante décrit comment les transports utilisent les méthodes TNEF pour traiter les messages sortants et entrants.
  
 **Pour envoyer un message qui inclut un flux TNEF**
  
1. Traitez les propriétés de message prises en charge par le système de messagerie.
    
2. Marquez le message d’une manière spécifique à l’implémentation afin que le fournisseur de transport de réception puisse déterminer que le message nécessite un traitement TNEF. Par exemple, un fournisseur de transport TNEF qui envoie à un système de messagerie SMTP peut ajouter un champ d’en-tête personnalisé tel que « X-CONTAINS-TNEF » pour indiquer que le message contient des données TNEF.
    
3. Obtenez un objet TNEF et utilisez-le pour encapsuler les propriétés de message non prises en charge par le système de messagerie dans un flux TNEF.
    
4. Encodez le flux TNEF à l’aide du modèle de pièce jointe du système de messagerie. Par exemple, si le modèle de pièce jointe sous-jacente consiste à uuencoder les pièces jointes et à les ajouter au texte du message, le fournisseur de transport doit uuencoder le flux TNEF dans une autre pièce jointe. Le fournisseur de transport doit également implémenter une méthode pour reconnaître la pièce jointe qui contient le flux TNEF encodé lorsqu’il reçoit un message. La méthode standard pour marquer cette pièce jointe consiste à lui attribuer le nom de fichier de pièce jointe « WINMAIL. DAT ». Si votre fournisseur de transport effectue cette opération, tous les autres fournisseurs de transport compatibles avec TNEF qui suivent cette convention pourront interagir avec lui.
    
5. Utilisez les méthodes d’interface [ITnef : IUnknown](itnefiunknown.md) pour insérer des balises décrivant les positions des pièces jointes de message dans le texte du message. 
    
6. Accédez au texte du message étiqueté par le biais des méthodes [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) et envoyez-le au système de messagerie. 
    
 **Pour récupérer les propriétés encapsulées**
  
1. Écrivez les propriétés prises en charge par le système de messagerie dans un nouveau message, y compris le texte du message étiqueté qui contient les propriétés encapsulées.
    
2. Décoder le flux TNEF à partir de la pièce jointe appropriée.
    
3. Décodez toutes les autres pièces jointes et écrivez-les dans les nouvelles pièces jointes MAPI d’un message.
    
4. Ouvrez le flux TNEF pour le décodage à l’aide de la fonction [OpenTnefStreamEx](opentnefstreamex.md) . 
    
5. Utilisez la méthode [ITnef::ExtractProps](itnef-extractprops.md) pour décoder le flux TNEF et écrire les propriétés encapsulées dans le nouveau message. Toutes les propriétés encodées qui sont des doublons de propriétés non codées remplacent les propriétés non codées lorsque les propriétés encodées sont décodées. 
    
6. Utilisez la méthode [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) pour analyser le texte du message afin de récupérer les positions des pièces jointes à partir des balises dans le texte du message. 
    

