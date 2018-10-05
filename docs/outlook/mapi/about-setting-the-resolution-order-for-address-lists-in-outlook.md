---
title: � propos de la d�finition de l'ordre de r�solution des listes d'adresses dans Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: 'Derni�re modification�: jeudi 5 juillet 2012'
ms.openlocfilehash: 07a4c3e90f686f291f95ff87f337b54d8bf35edc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391408"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a>� propos de la d�finition de l'ordre de r�solution des listes d'adresses dans Outlook

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour chaque profil, Microsoft Office Outlook prend en charge plusieurs listes d’adresses et les utilisateurs peuvent spécifier manuellement l’ordre des listes d’adresses par les destinataires de courrier électronique messages et les participants dans les demandes de réunion sont résolus. Par exemple, vous pouvez d�finir l'ordre de r�solution afin que les noms sont r�solus tout d'abord par rapport � votre carnet d'adresses Outlook, puis par rapport � la liste d'adresses globale. Sur un ordinateur, un utilisateur peut ouvrir le carnet d'adresses, cliquez sur **Outils**, puis sur **Options** pour sp�cifier l'ordre de r�solution. Toutefois, dans un environnement d'entreprise, il est plus efficace pour les administrateurs informatiques � d�finir par programme l'ordre des listes d'adresses par lequel les noms sont r�solus. Ce code peut �tre utilis� dans le cadre d'un script d'automation de d�marrage par un administrateur � l'int�rieur de l'entreprise. 
  
MAPI prend en charge la m�thode **[SetSearchPath](iaddrbook-getsearchpath.md)** dans l'interface **[IAddrBook](iaddrbookimapiprop.md)**, qui vous permet de d�finir un nouveau chemin d'acc�s de la recherche dans le profil qui est utilis� pour la r�solution de nom. Pour utiliser la m�thode **IAddrBook::SetSearchPath**, vous devez sp�cifier l'ordre de r�solution de votre choix � l'aide d'un tableau qui contient les conteneurs de l'adresse appropri�e de la documentation dans l'ordre, qu'ils doivent �tre r�solus. Chaque entr�e dans ce tableau doit �galement contenir l'identificateur d'entr�e du carnet d'adresses correspondant. 
  
Voici des exemples de code montrant comment sp�cifier un chemin de recherche personnalis� pour les listes d'adresses.
  
- [Définir par programme l’ordre de résolution des listes d’adresses](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [KB 292590 : comment faire pour modifier l'ordre de tri de carnet d'adresses avec SetSearchPath](https://support.microsoft.com/kb/292590)
    

