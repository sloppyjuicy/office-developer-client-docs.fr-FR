---
title: Traitement TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4d324fb3-d917-4502-b3a4-179c479deb79
description: 'Derni�re modification�: jeudi 5 juillet 2012'
ms.openlocfilehash: 7e194d5c23a092ee239d4efa3dad47b7dadb732c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624040"
---
# <a name="tnef-processing"></a>Traitement TNEF

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La série d’actions suivante décrit comment les transports utilisent les méthodes TNEF pour traiter les messages sortants et entrants.
  
 **Pour envoyer un message qui inclut un flux TNEF**
  
1. Traiter les propriétés de message qui sont pris en charge par le système de messagerie.
    
2. Marquez le message d’une manière spécifique à l’implémentation afin que le fournisseur de transport de réception puisse déterminer que le message nécessite un traitement TNEF. Par exemple, un fournisseur de transport TNEF envoyant un message à un système de messagerie SMTP peut ajouter un champ d’en-tête personnalisé tel que « X-CONTAINS-TNEF » pour indiquer que le message contient des données TNEF.
    
3. Obtenez un objet TNEF et utilisez-le pour encapsuler les propriétés de message non pris en charge par le système de messagerie dans un flux TNEF.
    
4. Encodez le flux TNEF à l’aide du modèle de pièce jointe du système de messagerie. Par exemple, si le modèle de pièce jointe sous-jacent consiste à uuencoder les pièces jointes et les ajoute au texte du message, le fournisseur de transport doit uuencoder le flux TNEF dans une autre pièce jointe. Le fournisseur de transport doit également implémenter une méthode pour reconnaître quelle pièce jointe contient le flux TNEF codé lorsqu’il reçoit un message. La manière standard de marquer cette pièce jointe consiste à lui donner le nom de fichier de pièce jointe « WINMAIL ». DAT ». Si votre fournisseur de transport le fait, tous les autres fournisseurs de transport activés pour le TNEF qui suivent cette convention pourront interopérer avec elle.
    
5. Utilisez [les méthodes d’interface ITnef : IUnknown](itnefiunknown.md) pour insérer des balises décrivant les positions des pièces jointes du message dans le texte du message. 
    
6. Accédez au texte du message balisé via [les méthodes IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) et envoyez-le au système de messagerie. 
    
 **Pour récupérer des propriétés encapsulées**
  
1. Écrivez les propriétés prise en charge par le système de messagerie dans un nouveau message, y compris le texte de message balisé qui contient les propriétés encapsulées.
    
2. Décodez le flux TNEF à partir de la pièce jointe appropriée.
    
3. Décodez les autres pièces jointes et écrivez-les dans les nouvelles pièces jointes MAPI d’un message.
    
4. Ouvrez le flux TNEF pour le décodage à l’aide de la [fonction OpenTnefStreamEx.](opentnefstreamex.md) 
    
5. Utilisez la [méthode ITnef::ExtractProps](itnef-extractprops.md) pour décoder le flux TNEF et écrire les propriétés encapsulées dans le nouveau message. Toutes les propriétés codées qui sont des doublons de propriétés non codées ont la valeur overwrite les propriétés non codées lorsque les propriétés codées sont décodées. 
    
6. Utilisez la [méthode ITnef::OpenTaggedBody](itnef-opentaggedbody.md) pour lire le texte du message afin de récupérer les positions des pièces jointes à partir des balises du texte du message. 
    

