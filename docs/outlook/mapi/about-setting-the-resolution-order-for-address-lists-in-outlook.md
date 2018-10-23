---
title: À propos de la définition de l’ordre de résolution pour les listes d’adresses dans Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: 'Dernière modification : 05 juillet 2012'
ms.openlocfilehash: 07a4c3e90f686f291f95ff87f337b54d8bf35edc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391408"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a>À propos de la définition de l’ordre de résolution pour les listes d’adresses dans Outlook

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour chaque profil, Microsoft Office Outlook prend en charge plusieurs listes d’adresses et les utilisateurs peuvent indiquer manuellement l’ordre des listes d’adresses dans lequel les destinataires des messages électroniques et les participants inclus dans les demandes de réunion sont résolus. Par exemple, vous pouvez définir l’ordre de résolution afin que les noms soient résolus en premier par rapport à votre carnet d’adresses Outlook, puis par rapport à la liste d’adresses globale. Sur un ordinateur, un utilisateur peut ouvrir le carnet d’adresses, cliquer sur **Outils**, puis sur **Options** pour indiquer l’ordre de résolution. Toutefois, dans un environnement d’entreprise, la solution la plus efficace pour les administrateurs informatiques consiste à définir par programmation l’ordre des listes d’adresses dans lequel les noms sont résolus. Ce type de code peut être utilisé dans le cadre d’un script d’automatisation du démarrage qu’un administrateur déploie au sein de l’entreprise. 
  
MAPI prend en charge la méthode **[SetSearchPath](iaddrbook-getsearchpath.md)** dans l’interface **[IAddrBook](iaddrbookimapiprop.md)**, ce qui vous permet de définir un nouveau chemin de recherche dans le profil utilisé pour la résolution de noms. Pour utiliser la méthode **IAddrBook::SetSearchPath**, vous devez indiquer l’ordre de résolution de votre choix à l’aide d’un tableau qui conserve les conteneurs des carnets d’adresses pertinents dans l’ordre dans lequel ils doivent être résolus. Chaque entrée de ce tableau doit également contenir l’ID d’entrée du carnet d’adresses correspondant. 
  
Voici quelques exemples de code de spécification de chemin de recherche personnalisé pour les listes d’adresses.
  
- [Programmation de l’ordre de résolution des listes d’adresses](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [Article 292590 de la base de connaissances : Procédure de modification de l’ordre de tri d’un carnet d’adresses avec SetSearchPath](https://support.microsoft.com/kb/292590)
    

