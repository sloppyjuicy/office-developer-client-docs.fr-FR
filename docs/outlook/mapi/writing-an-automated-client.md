---
title: Écriture d’un Client automatique
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8f9ac1a-b377-4f83-8fb6-ed85ab9053d0
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e5357c1e822dda35d3f38e00f91b58adbaf0ff9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787471"
---
# <a name="writing-an-automated-client"></a>Écriture d’un Client automatique

  
  
**S’applique à**: Outlook 
  
Une application cliente automatisée est une application qui s’exécute sans assistance, n’affichant aucun l’interface utilisateur.
  
 Par défaut, plusieurs méthodes d’interface MAPI affichent une interface utilisateur. Toutes ces méthodes ont des indicateurs qui autorisent un client autoriser ou supprimer cet affichage. Bien que MAPI attend des fournisseurs de services de respecter ces indicateurs, il existe certains fournisseurs qui ne remplissent pas toujours ces attentes. Une raison légitime ne pas en respectant les indicateurs est la dépendance du fournisseur de services sur un autre service qui n’autorise pas la suppression d’interface utilisateur. Si vous développez un client automatique, prêtez une attention particulière pour les fournisseurs de services que vous utilisez et la façon dont ils sont configurés. Ne pensez pas que tous vos appels pour supprimer une interface utilisateur sera réussi. 
  
Clients automatisées doivent avoir les informations nécessaires disponibles pour la configuration correcte de chacun des services de message dans le profil. Il existe deux méthodes pour fournir des informations de configuration au moment de l’ouverture de session :
  
- Le fournisseur de services peut récupérer les informations du profil.
    
- Le fournisseur de services peut demander à l’utilisateur pour plus d’informations. 
    
Dans la mesure où la deuxième option n’est pas disponible pour les clients automatisées, ces clients doivent utiliser la première option. Les clients doivent configurer leurs profils avec soin pour en garantir le fonctionne de cette option toujours.
  
Clients automatisées définir toujours l’indicateur MAPI_NO_MAIL dans l’appel de fonction [MAPILogonEx](mapilogonex.md) pour commencer une session MAPI. 
  

