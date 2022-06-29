---
title: � propos de la d�finition de l'ordre de r�solution des listes d'adresses dans Outlook
description: Décrit comment définir l’ordre de résolution des listes d’adresses par lesquelles les destinataires des messages électroniques et les participants aux demandes de réunion sont résolus dans Microsoft Outlook.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
ms.openlocfilehash: a1ec5de9634f0f34d6311782d839e38893e825f7
ms.sourcegitcommit: 1da753936975e64349cbd6954cf1c1732289a0b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2022
ms.locfileid: "66448615"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a>À propos de la définition de l’ordre de résolution pour les listes d’adresses dans Outlook

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour chaque profil, Microsoft Office Outlook prend en charge plusieurs listes d’adresses et les utilisateurs peuvent indiquer manuellement l’ordre des listes d’adresses dans lequel les destinataires des messages électroniques et les participants inclus dans les demandes de réunion sont résolus. Par exemple, vous pouvez définir l’ordre de résolution afin que les noms soient résolus en premier par rapport à votre carnet d’adresses Outlook, puis par rapport à la liste d’adresses globale. Sur un ordinateur, un utilisateur peut ouvrir le carnet d'adresses, cliquez sur **Outils**, puis sur **Options** pour sp�cifier l'ordre de r�solution. Toutefois, dans un environnement d'entreprise, il est plus efficace pour les administrateurs informatiques � d�finir par programme l'ordre des listes d'adresses par lequel les noms sont r�solus. Ce code peut �tre utilis� dans le cadre d'un script d'automation de d�marrage par un administrateur � l'int�rieur de l'entreprise. 
  
MAPI prend en charge la méthode **[SetSearchPath](iaddrbook-getsearchpath.md)** dans l’interface **[IAddrBook](iaddrbookimapiprop.md)**, ce qui vous permet de définir un nouveau chemin de recherche dans le profil utilisé pour la résolution de noms. Pour utiliser la méthode **IAddrBook::SetSearchPath**, vous devez indiquer l’ordre de résolution de votre choix à l’aide d’un tableau qui conserve les conteneurs des carnets d’adresses pertinents dans l’ordre dans lequel ils doivent être résolus. Chaque entrée de ce tableau doit également contenir l’ID d’entrée du carnet d’adresses correspondant. 
  
Voici quelques exemples de code de spécification de chemin de recherche personnalisé pour les listes d’adresses.
  
- [Programmation de l’ordre de résolution des listes d’adresses](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [Article 292590 de la base de connaissances : Procédure de modification de l’ordre de tri d’un carnet d’adresses avec SetSearchPath](/windows/win32/api/wabiab/nf-wabiab-iaddrbook-setsearchpath)
    

