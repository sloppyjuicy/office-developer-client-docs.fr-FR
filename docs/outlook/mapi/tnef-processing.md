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
ms.openlocfilehash: e6b3ef7c7eb469a5de909d440e22e522218a41f8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569490"
---
# <a name="tnef-processing"></a>Traitement TNEF

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
La série d’actions suivante décrire comment des transports utilisent les méthodes TNEF pour traiter les messages entrants et sortants.
  
 **Pour envoyer un message qui inclut un flux de données TNEF**
  
1. Traiter les propriétés des messages qui sont pris en charge par le système de messagerie.
    
2. Marquer le message dans une implémentation spécifique façon afin que le fournisseur de transport de réception peut déterminer que le message nécessite de traitement TNEF. Par exemple, un fournisseur de transport TNEF l’envoi à un serveur SMTP système de messagerie peut ajouter un champ d’en-tête personnalisé comme « X-contient-TNEF » pour indiquer que le message contient des données TNEF.
    
3. Obtenir un objet TNEF et utilisez-la pour encapsuler les propriétés de message non pris en charge par le système de messagerie dans un objet stream TNEF.
    
4. Coder le flux TNEF à l’aide du modèle de pièce jointe du système de messagerie. Par exemple, si le modèle de pièce jointe sous-jacent est uuencode des pièces jointes et les ajouter au texte du message, le fournisseur de transport doit uuencode le flux TNEF dans une autre pièce jointe. Le fournisseur de transport doit également implémenter une méthode pour reconnaître les pièces jointes contient le flux TNEF codé lorsqu’il reçoit un message. La méthode standard pour marquer cette pièce jointe est pour lui donner un nom de fichier des pièces jointes de « WINMAIL. DONNÉES ». Si votre fournisseur de transport pour cela, tous les fournisseurs de transport prenant en charge TNEF qui suivent cette convention sera en mesure d’interagir avec lui.
    
5. Utilisez [ITnef : IUnknown](itnefiunknown.md) méthodes pour insérer des balises décrivant les positions des pièces jointes des messages dans le texte du message de l’interface. 
    
6. Accès le texte du message avec balise via les méthodes [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) et l’envoyer au système de messagerie. 
    
 **Pour récupérer les propriétés encapsulées**
  
1. Écrire les propriétés prises en charge par le système de messagerie dans un nouveau message, y compris le texte du message avec balise qui contient les propriétés encapsulées.
    
2. Décoder le flux TNEF à partir de la pièce jointe appropriée.
    
3. Décoder toutes les pièces jointes et les écrire dans les nouvelles pièces jointes MAPI d’un message.
    
4. Ouvrez le flux TNEF de décodage à l’aide de la fonction [OpenTnefStreamEx](opentnefstreamex.md) . 
    
5. Utilisez la méthode [ITnef::ExtractProps](itnef-extractprops.md) pour décoder le flux TNEF et écrire les propriétés encapsulées dans le nouveau message. Les propriétés codées doublons des propriétés nonencoded remplace les propriétés nonencoded les propriétés codées sont décodées. 
    
6. Utilisez la méthode [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) pour analyser le texte du message pour récupérer les positions des pièces jointes dans les balises dans le texte du message. 
    

