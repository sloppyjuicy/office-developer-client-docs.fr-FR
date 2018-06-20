---
title: Cache du surnom dans
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2813c102-6778-4443-ab4b-b573f3568705
description: 'Dernière modification : 30 janvier 2013'
ms.openlocfilehash: 1ea1d3e6f636cf6a3ad47b6fdfe88d0f7130a5f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784907"
---
# <a name="nickname-cache"></a>Cache du surnom dans

 
  
**S’applique à**: Outlook 
  
Microsoft Office Outlook 2007, Microsoft Outlook 2010 et Microsoft Outlook 2013 interagissent avec le cache du surnom, également appelé « saisie semi-automatique flux. » Le flux de saisie semi-automatique est où Outlook persiste la liste de saisie semi-automatique, qui est la liste de noms qui s’affiche dans la zone **à**, **Cc**et **Cci** des zones d’édition pendant un utilisateur compose un message électronique. Cette rubrique décrit comment Outlook 2007, Outlook 2010 et Outlook 2013 interagissent avec le flux de saisie semi-automatique et traite également le format binaire du fichier et les méthodes recommandées pour interagir avec le flux de saisie semi-automatique. 
  
Pour les applications qui interagissent avec Outlook 2010 ou Outlook 2013, le flux de saisie semi-automatique est stocké sous forme d’une propriété MAPI et peut être modifié à l’aide de l’interface MAPI ou l’objet **PropertyAccessor** du message. L’objet **PropertyAccessor** est exposé dans les modèles objet Outlook 2010 ou Outlook 2013. 
  
Il n’existe aucune dépendance sur le modèle objet Outlook 2007 ou des API de MAPI. Par conséquent, les applications qui effectuent des modifications dans le flux de saisie semi-automatique dans Outlook 2007 peuvent être écrites à l’aide de n’importe quel langage de programmation.
  
## <a name="interacting-with-the-autocomplete-stream"></a>Interaction avec le flux de saisie semi-automatique

Lorsque les zones d’édition **à**, **Cc**ou **Cci** sont accessibles dans un message, le flux de saisie semi-automatique est chargé et la liste des noms d’utilisateur s’affiche. Outlook interagit avec le flux de saisie semi-automatique de deux manières : 
  
1. Chargement du flux de saisie semi-automatique 
    
2. Enregistrer les modifications de données dans le flux de saisie semi-automatique
    
Le moyen de stocker les données de saisie semi-automatique diffère entre Outlook 2007 et Outlook 2010 ou Outlook 2013 comme suit : 
  
 **Outlook 2007**
  
Pour Outlook 2007, le flux de saisie semi-automatique est stocké dans un fichier avec le même nom que le profil et d’une extension .nk2. Par exemple, si le profil par défaut de « outlook » est utilisé, le fichier sera appelé « outlook.nk2 ». Le fichier .nk2 est stocké dans % APPDATA%\Microsoft\Outlook. Pour plus d’informations sur le format de fichier binaire surnom du cache, voir [Format de fichier NK2 Outlook 2003/2007 et des instructions pour les développeurs](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf).
  
 **Outlook 2010 et Outlook 2013**
  
Outlook 2010 ou Outlook 2013 lit le flux de saisie semi-automatique à partir d’un message dans le tableau contenu associé de la boîte de réception de la banque de remise du compte de messagerie. Ce message masqué a une classe de message et l’objet de IPM. Configuration.Autocomplete. Le flux de saisie semi-automatique est stocké sur ce message dans la propriété PR_ROAMING_BINARYSTREAM ([Propriété canonique PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)). Les données de saisie semi-automatique peuvent être temporairement mis en cache dans un fichier .dat de saisie semi-automatique dans % USERPROFILE%\AppData\Local\Microsoft\Outlook\RoamCache. Toutefois, le fichier .dat uniquement un cache et n’est pas utilisé pour écrire dans la banque de remise lorsque l’utilisateur quitte Outlook 2010 ou Outlook 2013.
  
## <a name="loading-the-autocomplete-stream"></a>Chargement du flux de saisie semi-automatique

Outlook charge le flux de saisie semi-automatique chaque fois qu’un élément avec la fonctionnalité d’adressage est initialisé. Par exemple, les adresses de messagerie sont utilisés dans un nouveau message, une réponse à un message, un élément de contact, une demande de réunion et ainsi de suite. Pour charger les données, il lit tout le contenu de l’objet stream en mémoire.
  
Pour les opérations de saisie semi-automatique, Outlook interagit avec cette structure en mémoire uniquement pendant la durée de la durée du processus outlook.exe. Outlook enregistre uniquement la structure de l’arrêt. Voir la section suivante « L’enregistrement du flux de saisie semi-automatique » pour plus d’informations sur ce processus.
  
## <a name="saving-the-autocomplete-stream"></a>L’enregistrement du flux de saisie semi-automatique

Outlook enregistre le flux de saisie semi-automatique lors de l’arrêt si la liste de saisie semi-automatique a changé dans une des manières suivantes :
  
- Une nouvelle entrée de surnom est ajoutée par le biais de résolution d’un nom, sélectionner un destinataire à partir de la boîte de dialogue de carnet d’adresse ou l’envoi du courrier à un destinataire qui n’est pas déjà dans la liste.
    
- Une entrée est modifiée en envoyant un message à un destinataire existant dans la liste.
    
- Suppression d’une entrée par l’utilisateur via l’interface utilisateur.
    
- Autres scénarios secondaires non pertinents pour cette rubrique.
    
Enregistrer les modifications dans les données de saisie semi-automatique implique la réécriture de la structure en mémoire à un [flux de saisie semi-automatique](autocomplete-stream.md). Lors de l’interaction avec Outlook 2007, le flux est enregistré dans un fichier local .nk2. Pour Outlook 2010 ou Outlook 2013, le flux de saisie semi-automatique écrit dans le tableau contenu associé de la boîte de réception de la banque de remise du compte de messagerie.
  
## <a name="recommendations"></a>Recommandations

- Ne jamais partiellement modifier le flux de saisie semi-automatique. L’interaction pris en charge est de 1) lire le flux de saisie semi-automatique entier en mémoire, (2) modifier la structure de la mémoire et (3) réécrire l’intégralité du flux soit le tableau associé le contenu de la boîte de réception de la banque de remise du compte de messagerie (pour Outlook 2010 ou Outlook 2013) ou sur le fichier .nk2 local (Outlook 2007).
    
- Sans interaction avec le flux de saisie semi-automatique pendant l’exécution d’Outlook. Si Outlook est en cours d’exécution lors de la modification du flux, il remplace probablement vos modifications lorsqu’il arrête.
    
- Ne pas les propriétés d’écriture de tapent PT_MV_UNICODE et PR_MV_STRING8 dans un flux de saisie semi-automatique pour être utilisées par Microsoft Outlook 2003. Ces propriétés sont uniquement comprises par Outlook 2007, Outlook 2010 et Outlook 2013.
    
- Lors du développement de code qui interagit avec Outlook 2007, nous vous recommandons de verrouiller le fichier .nk2 contre toute modification par d’autres processus pendant que vous êtes lecture et écriture à l’aide des API (par exemple, **fichier de verrouillage** dans C/C++ et **le verrouillage de fichier standard FileStream.Lock** en c#). 
    
- Uniquement modifier les propriétés des types de l’ensemble de lignes de l’objet stream de saisie semi-automatique. Pour plus d’informations sur les propriétés de flux de saisie semi-automatique et les types de propriétés, voir [flux de saisie semi-automatique](autocomplete-stream.md).
    
## <a name="see-also"></a>Voir aussi



[Flux de saisie semi-automatique](autocomplete-stream.md)
  
[Profils MAPI](mapi-profiles.md)


[Format de fichier NK2 Outlook 2003/2007 et des instructions pour les développeurs](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)

