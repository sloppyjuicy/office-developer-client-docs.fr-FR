---
title: Configuration de DataFactory en mode sans échec ou non restreint
TOCTitle: Configuring DataFactory for Safe or Unrestricted Modes
ms:assetid: 1516068f-1b02-3236-f6a9-9fdeff098e52
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248915(v=office.15)
ms:contentKeyID: 48543400
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4f3658f3fdefeb87813319e4ed0313fe5c6032cf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882265"
---
# <a name="configuring-datafactory-for-safe-or-unrestricted-modes"></a><span data-ttu-id="52711-102">Configuration de DataFactory en mode sans échec ou non restreint</span><span class="sxs-lookup"><span data-stu-id="52711-102">Configuring DataFactory for Safe or Unrestricted Modes</span></span>


<span data-ttu-id="52711-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="52711-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="52711-p101">ADO est installé par défaut avec une configuration [RDSServer.DataFactory](datafactory-object-rdsserver.md) « sécurisée ». Pour que les composants serveur de RDS s'exécutent en mode sans échec, les conditions suivantes doivent être satisfaites :</span><span class="sxs-lookup"><span data-stu-id="52711-p101">By default, ADO is installed with a "safe" [RDSServer.DataFactory](datafactory-object-rdsserver.md) configuration. Safe mode for RDS Server components means that the following are true:</span></span>

1.  <span data-ttu-id="52711-106">Un gestionnaire est requis avec l'objet RDSServer.DataFactory (imposé par le paramétrage d'une clé de Registre).</span><span class="sxs-lookup"><span data-stu-id="52711-106">Handler is required with the RDSServer.DataFactory (this is mandated by a registry key setting).</span></span>

2.  <span data-ttu-id="52711-107">Le gestionnaire msdfmap.handler est inscrit, figure dans la liste de gestionnaires sécurisés et est marqué comme gestionnaire par défaut.</span><span class="sxs-lookup"><span data-stu-id="52711-107">The default handler, msdfmap.handler, is registered, present in the safe-handler list, and marked as the default handler.</span></span>

3.  <span data-ttu-id="52711-p102">Le fichier Msdfmap.ini est installé dans le répertoire Windows. Vous devez le configurer le cas échéant avant d'utiliser RDS en mode d'application à trois niveaux.</span><span class="sxs-lookup"><span data-stu-id="52711-p102">Msdfmap.ini file is installed in the Windows directory. You must configure this file according to your needs, before using RDS in three-tier mode.</span></span>

<span data-ttu-id="52711-110">Vous pouvez éventuellement configurer une installation de **DataFactory** en mode non restreint.</span><span class="sxs-lookup"><span data-stu-id="52711-110">Optionally, you can configure an unrestricted **DataFactory** installation.</span></span> <span data-ttu-id="52711-111">**DataFactory** peut être utilisé directement sans le gestionnaire personnalisé.</span><span class="sxs-lookup"><span data-stu-id="52711-111">**DataFactory** can be used directly without the custom handler.</span></span> <span data-ttu-id="52711-112">Les utilisateurs peuvent néanmoins utiliser ce dernier en modifiant les chaînes de connexion, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="52711-112">Users can still use a custom handler by modifying the connection strings, but it is not required.</span></span> <span data-ttu-id="52711-113">Pour plus d’informations sur les implications de l’utilisation de l’objet **RDSServer.DataFactory** , consultez [Sécurisation des Applications RDS](securing-rds-applications.md).</span><span class="sxs-lookup"><span data-stu-id="52711-113">For more information about the implications of using the **RDSServer.DataFactory** object, see [Securing RDS Applications](securing-rds-applications.md).</span></span>

<span data-ttu-id="52711-p104">Le fichier de Registre handsafe.reg est fourni afin de configurer les entrées de Registre du gestionnaire et obtenir ainsi une configuration sécurisée. Pour fonctionner en mode sans échec, exécutez handsafe.reg. Le fichier de Registre handunsf.reg est quant à lui fourni pour configurer les entrées de Registre du gestionnaire afin de bénéficier d'une configuration sans restriction d'accès. Pour fonctionner en mode non restreint, exécutez le fichier handunsf.reg.</span><span class="sxs-lookup"><span data-stu-id="52711-p104">The registry file handsafe.reg has been provided to set up the handler registry entries for a safe configuration. To run in safe mode, run handsafe.reg. The registry file handunsf.reg has been provided to set up the handler registry entries for an unrestricted configuration. To run in unrestricted mode, run handunsf.reg.</span></span>

<span data-ttu-id="52711-117">Après l’exécution de handsafe.reg ou handunsf.reg, vous devez arrêter et redémarrer le Service de publication World Wide Web sur le serveur web en tapant les commandes suivantes dans une fenêtre de commande : « NET STOP W3SVC » et « NET démarrer W3SVC ».</span><span class="sxs-lookup"><span data-stu-id="52711-117">After running either handsafe.reg or handunsf.reg, you must stop and restart the World Wide Web Publishing Service on the web server by typing the following commands in a command window: "NET STOP W3SVC" and "NET START W3SVC".</span></span>

<span data-ttu-id="52711-118">Pour plus d'informations sur l'utilisation de la fonctionnalité du gestionnaire de personnalisation RDS, consultez l'article technique en anglais « Using the Customization Handler Feature in RDS 2.1 ».</span><span class="sxs-lookup"><span data-stu-id="52711-118">For more information about using the customization handler feature of RDS, see the technical article Using the Customization Handler Feature in RDS 2.1.</span></span>

