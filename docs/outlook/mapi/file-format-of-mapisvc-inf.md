---
title: Format de fichier du fichier MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b48eda17-83a8-4dc4-85c8-4ca827d13d25
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 47b698eb12577442e5b2d9ea9ecae3e8a13e402b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783299"
---
# <a name="file-format-of-mapisvcinf"></a>Format de fichier du fichier MapiSvc.inf

**S’applique à**: Outlook 
  
La base de données centrale pour les informations de configuration de service de message MAPI joue le rôle du fichier MapiSvc.inf. MapiSvc.inf contient des informations sur chacun des services message installés sur la station de travail, plus d’informations sur les fournisseurs de services qui appartiennent à chaque service de message et des informations sur le sous-système MAPI. MapiSvc.inf est la source principale des informations de profils. Autrement dit, lors de la génération d’un nouveau profil ou un modifié, les informations pertinentes pour chaque service de message ou fournisseur de services est copié à partir du fichier MapiSvc.inf. 
  
MapiSvc.inf est divisée en sections hiérarchiques liées :
  
1. Section contenant des informations qui s’applique à tous les profils. Cette section comporte trois parties :
    
   - Section **[services]** , fournissant des liens vers chaque le message suivant sections de service. 
    
   - **[Help File Mappings]** section, contenant des informations sur. Fichiers HLP fournis par les services de messagerie. 
    
   - Section **[Services par défaut]** , répertoriant les services de messagerie qui composent une installation par défaut. 
    
2. Section contenant des informations qui s’applique aux services de messagerie spécifique. Entrées dans les sections suivantes fournissent des liens vers des sections de fournisseur de service suivantes.
    
3. Section contenant des informations qui s’applique aux fournisseurs de services individuels dans un service de message.
    
L’illustration suivante montre l’organisation du fichier MapiSvc.inf classique. Il existe trois services de messagerie : AB, MsgService et MS. Le nom sur le côté droit du signe égal pour chaque service de message est le nom d’affichage du service. Chaque service de message possède sa propre section ailleurs dans le fichier qui est lié à une ou plusieurs sections de fournisseur de service. Il existe une section de fournisseur de service pour chaque fournisseur de service qui appartient au service de message. Les carnet d’adresses et MS message services sont fournisseur unique tandis que les trois fournisseurs de services appartiennent au service MsgService.
  
**Organisation du fichier MapiSvc.inf**
  
![Organisation du fichier MapiSvc.inf] (media/amapi_30.gif "Organisation du fichier MapiSvc.inf")
  
MAPI fournit une version de base du fichier MapiSvc.inf qui contient les entrées pour le sous-système MAPI. Chaque implémentation de service de message ajoute des entrées qui conviennent à la fois pour leur service et les fournisseurs de services qui appartiennent à leur service. Certaines entrées sont requis pendant que d’autres sont facultatifs. Par exemple, MAPI nécessite que vous spécifiez le nom et le chemin d’accès de chacun des fournisseurs de services dans votre service de message. Sans ces informations, ils ne peuvent pas être chargés.
  
Vous pouvez ajouter des informations obligatoires et facultatifs dans la section de votre service de message et/ou les sections de fournisseur de service. Où placer les informations de votre service de message dépend du nombre de fournisseurs de services dans le service. Étant donné que ces informations s’appliquent à chaque fournisseur de services dans le service, vous devez le rendre accessible à tous les fournisseurs. Stocker dans la section service de message, l’option par défaut, ou dans toutes les sections de fournisseur de service. Stocker les informations une fois pour éviter les réplications inutiles et la nécessité de conserver plusieurs copies synchronisés.
  
Si votre service de message est un service de fournisseur unique, stocker toutes les informations de service de message dans la section pour le fournisseur de services plutôt que dans la section pour le service. Accès à la section fournisseur de service est plus rapide et plus directe que l’accès à la section service de message. 
  
Stocker uniquement les données de configuration public dans le fichier MapiSvc.inf. Informations privé ou requiert une protection supplémentaire, tels que les mots de passe ou d’autres informations d’identification, ne doivent pas être incluses dans ce fichier. Adhésion au lieu de cela, pas pour stocker les informations de ce type tout ou conserver dans le profil en tant que propriétés sécurisées. Propriétés sécurisées ont des fonctionnalités de protection intégrés tels que le chiffrement.
  

