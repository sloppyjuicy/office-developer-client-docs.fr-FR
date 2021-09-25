---
title: Cache de surnoms
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 2813c102-6778-4443-ab4b-b573f3568705
description: 'Last modified: January 30, 2013'
ms.openlocfilehash: 6c1074086f4aec413c09fdfe3ca8e7b879f083e4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579452"
---
# <a name="nickname-cache"></a>Cache de surnoms

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Microsoft Office Outlook 2007, Microsoft Outlook 2010 et Microsoft Outlook 2013 interagissent avec le cache de surnoms, également appelé « flux de mise à jour automatique ». Le flux de mise à jour automatique est l’endroit où Outlook fait persister la liste de la  mise à jour automatique, qui est la liste des noms qui s’affiche dans les zones d’édition À **,** **Cc** et Cci pendant qu’un utilisateur compose un e-mail. Cette rubrique décrit la façon dont Outlook 2007, Outlook 2010 et Outlook 2013 interagissent avec le flux de la mise àcomplet automatique et traite également du format binaire du fichier et des méthodes recommandées pour interagir avec ce flux. 
  
Pour les applications qui interagissent avec Outlook 2010 ou Outlook 2013, le flux de mise à jour automatique est stocké en tant que propriété MAPI et peut être modifié à l’aide de l’objet MAPI ou **PropertyAccessor** du message. **L’objet PropertyAccessor** est exposé dans Outlook 2010 ou Outlook 2013. 
  
Il n’existe aucune dépendance sur le modèle Outlook 2007 ou les API MAPI. Par conséquent, les applications qui modifient le flux de la mise à jour automatique dans Outlook 2007 peuvent être écrites à l’aide de n’importe quel langage de programmation.
  
## <a name="interacting-with-the-autocomplete-stream"></a>Interaction avec le flux decomplet automatique

Lorsque les zones d’édition **À,** **Cc** ou **Cci** sont accessibles sur un message, le flux de mise à jour automatique est chargé et la liste des noms d’utilisateurs s’affiche. Outlook interagit avec le flux de la mise à jour automatique de deux manières : 
  
1. Chargement du flux decomplete automatique 
    
2. Enregistrement des modifications apportées aux données dans le flux decomplet automatique
    
Le stockage des données de la mise à jour automatique diffère entre Outlook 2007 et Outlook 2010 ou Outlook 2013 comme suit : 
  
 **Outlook 2007**
  
Pour Outlook 2007, le flux de la mise à jour automatique est stocké dans un fichier avec le même nom que le profil et une extension de .nk2. Par exemple, si le profil par défaut de « outlook » est utilisé, le fichier sera appelé « outlook.nk2 ». Le fichier .nk2 est stocké dans %APPDATA%\Microsoft\Outlook. Pour plus d’informations sur le format de fichier binaire du cache de surnoms, voir [Outlook 2003/2007 NK2 File Format and Developer Guidelines](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf).
  
 **Outlook 2010 et Outlook 2013**
  
Outlook 2010 ou Outlook 2013 lit le flux de la mise à correspondance automatique à partir d’un message dans la table Contenu associé de la boîte de réception de la banque de remise du compte de messagerie. Ce message masqué a une classe de message et l’objet de IPM. Configuration.Autocomplete. Le flux de mise à jour automatique est stocké sur ce message dans la propriété PR_ROAMING_BINARYSTREAM ( Propriété canonique[PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)). Les données de la mise en cache automatique peuvent être temporairement mises en cache dans un fichier .dat de mise à jour automatique situé dans %USERPROFILE%\AppData\Local\Microsoft\Outlook\RoamCache. Toutefois, le fichier .dat n’est qu’un cache et n’est pas utilisé pour écrire dans le magasin de remise lorsque l’utilisateur quitte Outlook 2010 ou Outlook 2013.
  
## <a name="loading-the-autocomplete-stream"></a>Chargement du flux de la mise àcomplet automatique

Outlook charge le flux de saisiecomplet automatique chaque fois qu’un élément avec la fonctionnalité d’adressaing est initialisé. Par exemple, les adresses de messagerie sont utilisées dans un nouveau courrier, une réponse à un message, un élément de contact, une demande de réunion, etc. Pour charger les données, Outlook lit tout le contenu du flux dans la mémoire.
  
Pour les opérations de mise à Outlook, les utilisateurs interagissent exclusivement avec cette structure en mémoire pendant toute la durée outlook.exe durée de vie du processus. Outlook enregistre uniquement la structure à l’arrêt. Pour plus d’informations sur ce processus, voir la section suivante « Enregistrement du flux de mise à jour automatique ».
  
## <a name="saving-the-autocomplete-stream"></a>Enregistrement du flux de la mise àcomplet automatique

Outlook enregistre le flux de mise à jour automatique à l’arrêt si la liste de la mise à jour automatique a été modifiée de l’une des manières suivantes :
  
- Une nouvelle entrée de surnom est ajoutée en résolvant un nom, en sélectionnant un destinataire dans la boîte de dialogue du carnet d’adresses ou en envoyant un message à un destinataire qui n’était pas déjà dans la liste.
    
- Une entrée est modifiée en envoyant un message électronique à un destinataire existant dans la liste.
    
- Une entrée est supprimée par l’utilisateur via l’interface utilisateur.
    
- Autres scénarios mineurs non pertinents pour cette rubrique.
    
L’enregistrement des modifications apportées aux données de lacomplet automatique implique l’écriture de la structure en mémoire dans un flux [de la mise àcomplet automatique.](autocomplete-stream.md) Lors de l’interaction Outlook 2007, le flux est enregistré dans un fichier .nk2 local. Pour Outlook 2010 ou Outlook 2013, le flux decomplet automatique écrit dans la table Contenu associé de la boîte de réception de la banque de remise du compte de messagerie.
  
## <a name="recommendations"></a>Recommandations

- Ne modifiez jamais partiellement le flux decomplet automatique. L’interaction prise en charge est de 1) lire l’intégralité du flux de lacomplete automatique dans la mémoire, 2) modifier la structure de la mémoire et 3) écrire l’intégralité du flux dans la table Contenu associé de la boîte de réception de la banque de remise du compte de messagerie (pour Outlook 2010 ou Outlook 2013) ou dans le fichier .nk2 local (Outlook 2007).
    
- N’interagissez pas avec le flux de la mise à Outlook en cours d’exécution. Si Outlook est en cours d’exécution pendant que vous modifiez le flux, il est probable qu’il est en cours d’exécution pour modifier vos modifications lors de son arrêt.
    
- N’écrivez pas les propriétés de type PT_MV_UNICODE et PR_MV_STRING8 dans un flux de mise àcomplet automatique à consommer par Microsoft Outlook 2003. Ces propriétés sont comprises uniquement par Outlook 2007, Outlook 2010 et Outlook 2013.
    
- Lorsque vous développez du code qui interagit avec Outlook 2007, nous vous recommandons de verrouiller le fichier .nk2 d’une modification par d’autres processus pendant que vous l’lisez et l’écrivez à l’aide des API de verrouillage de fichier standard (par exemple, **LockFile** en C/C++ et **FileStream.Lock** dans C#). 
    
- Modifiez uniquement les propriétés des types qui sont issus du jeu de lignes du flux de mise à jour automatique. Pour plus d’informations sur les propriétés et les types de propriétés de flux de lacomplete automatique, voir [Flux de lacomplet automatique.](autocomplete-stream.md)
    
## <a name="see-also"></a>Voir aussi



[Autocomplete Stream](autocomplete-stream.md)
  
[Profils MAPI](mapi-profiles.md)


[Outlook 2003/2007 NK2 File Format and Developer Guidelines](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)

