---
title: Cache de surnoms
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2813c102-6778-4443-ab4b-b573f3568705
description: 'Dernière modification: 30 janvier 2013'
ms.openlocfilehash: 841b01ae8dfcf841b0a1d64113ce7258c4c61583
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334516"
---
# <a name="nickname-cache"></a>Cache de surnoms

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Microsoft Office Outlook 2007, Microsoft Outlook 2010 et Microsoft Outlook 2013 interagissent avec le cache des surnoms, également appelé «flux de saisie semi-automatique». Le flux de saisie semi-automatique est l'emplacement où Outlook conserve la liste de saisie semi-automatique, qui est la liste des noms qui s'affichent dans les zones **d'édition à**, **CC**et **CCI** pendant qu'un utilisateur compose un message électronique. Cette rubrique décrit comment Outlook 2007, Outlook 2010 et Outlook 2013 interagissent avec le flux de saisie semi-automatique et décrit également le format binaire du fichier et les méthodes recommandées pour interagir avec le flux de saisie semi-automatique. 
  
Pour les applications qui interagissent avec Outlook 2010 ou Outlook 2013, le flux de saisie semi-automatique est stocké en tant que propriété MAPI et peut être modifié à l'aide de l'objet MAPI ou **propertyAccessor** du message. L'objet **propertyAccessor** est exposé dans les modèles d'objet Outlook 2010 ou Outlook 2013. 
  
Il n'existe aucune dépendance vis-à-vis du modèle objet ou des API MAPI Outlook 2007. Par conséquent, les applications qui apportent des modifications au flux de saisie semi-automatique dans Outlook 2007 peuvent être écrites à l'aide de n'importe quel langage de programmation.
  
## <a name="interacting-with-the-autocomplete-stream"></a>Interaction avec le flux de saisie semi-automatique

Lorsque vous accédez aux zones **d'édition à**, **CC**ou **CCI** sur un message, le flux de saisie semi-automatique est chargé et la liste des noms d'utilisateur s'affiche. Outlook interagit avec le flux de saisie semi-automatique de deux manières: 
  
1. Chargement du flux de saisie semi-automatique 
    
2. Enregistrement des modifications apportées aux données dans le flux de saisie semi-automatique
    
Les moyens de stocker les données de saisie semi-automatique diffèrent entre Outlook 2007 et Outlook 2010 ou Outlook 2013 comme suit: 
  
 **Outlook 2007**
  
Pour Outlook 2007, le flux de saisie semi-automatique est stocké dans un fichier portant le même nom que le profil et une extension. NK2. Par exemple, si le profil par défaut «Outlook» est utilisé, le fichier est appelé «Outlook. NK2». Le fichier. nk2 est stocké dans%APPDATA%\Microsoft\Outlook. Pour plus d'informations sur le format de fichier binaire du cache des surnoms, consultez le [format de fichier NK2 Outlook 2003/2007 et les instructions](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)pour les développeurs.
  
 **Outlook 2010 et Outlook 2013**
  
Outlook 2010 ou Outlook 2013 lit le flux de saisie semi-automatique à partir d'un message dans le tableau contenu associé de la boîte de réception du magasin de remise du compte de messagerie. Ce message masqué a une classe de message et l'objet de IPM. Configuration. AutoComplete. Le flux de saisie semi-automatique est stocké sur ce message dans la propriété PR_ROAMING_BINARYSTREAM ([propriété canonique PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)). Les données de saisie semi-automatique peuvent être temporairement mises en cache dans un fichier AutoComplete. dat situé dans%USERPROFILE%\AppData\Local\Microsoft\Outlook\RoamCache. Toutefois, le fichier. dat n'est qu'un cache et n'est pas utilisé pour effectuer une réécriture dans le magasin de remise lorsque l'utilisateur quitte Outlook 2010 ou Outlook 2013.
  
## <a name="loading-the-autocomplete-stream"></a>Chargement du flux de saisie semi-automatique

Outlook charge le flux de saisie semi-automatique chaque fois qu'un élément avec une fonctionnalité d'adressage est initialisé. Par exemple, les adresses de messagerie sont utilisées dans un nouveau message électronique, une réponse de messagerie, un élément de contact, une demande de réunion, etc. Pour charger les données, Outlook lit tout le contenu du flux dans la mémoire.
  
Pour les opérations de saisie semi-automatique, Outlook interagit exclusivement avec cette structure en mémoire pendant la durée de la durée de vie du processus Outlook. exe. Outlook enregistre uniquement la structure lors de l'arrêt. Consultez la section suivante «enregistrement du flux de saisie semi-automatique» pour plus d'informations sur ce processus.
  
## <a name="saving-the-autocomplete-stream"></a>Enregistrement du flux de saisie semi-automatique

Outlook enregistre le flux de saisie semi-automatique lors de l'arrêt si la liste de saisie semi-automatique a été modifiée de l'une des manières suivantes:
  
- Une nouvelle entrée de surnom est ajoutée par la résolution d'un nom, le choix d'un destinataire dans la boîte de dialogue Carnet d'adresses ou l'envoi d'un message à un destinataire qui ne figure pas déjà dans la liste.
    
- Une entrée est modifiée par l'envoi d'un courrier électronique à un destinataire existant dans la liste.
    
- Une entrée est supprimée par l'utilisateur via l'interface utilisateur.
    
- Autres scénarios mineurs non pertinents pour cette rubrique.
    
L'enregistrement des modifications apportées aux données de saisie semi-automatique implique l'écriture de la structure en mémoire dans un [flux de saisie semi-automatique](autocomplete-stream.md). Lors de l'interaction avec Outlook 2007, le flux est enregistré dans un fichier. nk2 local. Pour Outlook 2010 ou Outlook 2013, le flux de saisie semi-automatique est réécrit dans le tableau contenu associé de la boîte de réception du magasin de remise du compte de messagerie.
  
## <a name="recommendations"></a>Recommandations

- Ne modifiez jamais partiellement le flux de saisie semi-automatique. L'interaction prise en charge est de 1) lire l'intégralité du flux de saisie semi-automatique dans la mémoire, 2) modifier la structure de la mémoire et 3) écrire l'ensemble du flux dans le tableau contenu associé de la boîte de réception du magasin de remise du compte de messagerie (pour Outlook 2010 ou Outlook 2013) ou au fichier. nk2 local (Outlook 2007).
    
- N'interagissez pas avec le flux de saisie semi-automatique Quand Outlook est en cours d'exécution. Si Outlook est en cours d'exécution pendant que vous modifiez le flux, il remplacera probablement vos modifications lors de l'arrêt.
    
- N'écrivez pas les propriétés de type PT_MV_UNICODE et PR_MV_STRING8 dans un flux de saisie semi-automatique devant être utilisé par Microsoft Outlook 2003. Ces propriétés sont uniquement comprises par Outlook 2007, Outlook 2010 et Outlook 2013.
    
- Lorsque vous développez du code qui interagit avec Outlook 2007, nous vous recommandons de verrouiller le fichier. nk2 contre les modifications apportées par d'autres processus lors de la lecture et de l'écriture à l'aide d'API de verrouillage de fichier standard (par exemple, **lockfile** dans C/C++ et ** FileStream. Lock** en C#). 
    
- Modifiez uniquement les propriétés des types provenant de l'ensemble de lignes du flux de saisie semi-automatique. Pour plus d'informations sur les propriétés et les types de propriétés du flux de saisie semi-automatique, voir AutoComplete [Stream](autocomplete-stream.md).
    
## <a name="see-also"></a>Voir aussi



[Flux de saisie semi-automatique](autocomplete-stream.md)
  
[Profils MAPI](mapi-profiles.md)


[Format de fichier NK2 Outlook 2003/2007 et conseils pour les développeurs](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)

