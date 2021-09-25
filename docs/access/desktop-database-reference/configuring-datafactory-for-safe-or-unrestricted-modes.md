---
title: Configuration de DataFactory en mode sans échec ou non restreint
TOCTitle: Configuring DataFactory for Safe or Unrestricted Modes
ms:assetid: 1516068f-1b02-3236-f6a9-9fdeff098e52
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248915(v=office.15)
ms:contentKeyID: 48543400
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: aa371dd98d61bd23b33c83bf4ce9b78947e10600
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577562"
---
# <a name="configuring-datafactory-for-safe-or-unrestricted-modes"></a>Configuration de DataFactory en mode sans échec ou non restreint


**S’applique à** : Access 2013, Office 2013

ADO est installé par défaut avec une configuration [RDSServer.DataFactory](datafactory-object-rdsserver.md) « sécurisée ». Pour que les composants serveur de RDS s'exécutent en mode sans échec, les conditions suivantes doivent être satisfaites :

1.  Un gestionnaire est requis avec l'objet RDSServer.DataFactory (imposé par le paramétrage d'une clé de Registre).

2.  Le gestionnaire msdfmap.handler est inscrit, figure dans la liste de gestionnaires sécurisés et est marqué comme gestionnaire par défaut.

3.  Le fichier Msdfmap.ini est installé dans le répertoire Windows. Vous devez le configurer le cas échéant avant d'utiliser RDS en mode d'application à trois niveaux.

Vous pouvez éventuellement configurer une installation de **DataFactory** en mode non restreint. **DataFactory** peut être utilisé directement sans le gestionnaire personnalisé. Les utilisateurs peuvent néanmoins utiliser ce dernier en modifiant les chaînes de connexion, le cas échéant. Pour plus d’informations sur les implications de l’utilisation de l’objet **RDSServer.DataFactory,** voir [Sécurisation des applications RDS.](securing-rds-applications.md)

Le fichier de Registre handsafe.reg est fourni afin de configurer les entrées de Registre du gestionnaire et obtenir ainsi une configuration sécurisée. Pour fonctionner en mode sans échec, exécutez handsafe.reg. Le fichier de Registre handunsf.reg est quant à lui fourni pour configurer les entrées de Registre du gestionnaire afin de bénéficier d'une configuration sans restriction d'accès. Pour fonctionner en mode non restreint, exécutez le fichier handunsf.reg.

Après avoir exécutez handsafe.reg ou handunsf.reg, vous devez arrêter et redémarrer le service de publication World Wide Web sur le serveur web en tapant les commandes suivantes dans une fenêtre de commande : « NET STOP W3SVC » et « NET START W3SVC ».

Pour plus d'informations sur l'utilisation de la fonctionnalité du gestionnaire de personnalisation RDS, consultez l'article technique en anglais « Using the Customization Handler Feature in RDS 2.1 ».

