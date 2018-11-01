---
title: Configuration de RDS sur Windows 2000
TOCTitle: Configuring RDS on Windows 2000
ms:assetid: eb2d4c1d-8b3b-07ac-258f-edb0b1a3daba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250193(v=office.15)
ms:contentKeyID: 48548482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2a02db4af012bb7eb0b297d93ef35ba3fc0bd90c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883595"
---
# <a name="configuring-rds-on-windows-2000"></a><span data-ttu-id="f7579-102">Configuration de RDS sur Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f7579-102">Configuring RDS on Windows 2000</span></span>


<span data-ttu-id="f7579-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7579-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f7579-104">Si vous rencontrez des difficultés pour faire fonctionner RDS correctement après avoir effectué une mise à niveau vers Windows 2000, suivez les étapes ci-dessous pour tenter de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="f7579-104">If you experience difficulties getting RDS to function properly after upgrading to Windows 2000, follow the steps below to troubleshoot the issue.</span></span>

1.  <span data-ttu-id="f7579-105">Assurez-vous que le premier que le Service de publication World Wide Web est en cours d’exécution en accédant à https://*server* à l’aide d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f7579-105">Make sure that the World Wide Web Publishing Service is running first by navigating to https://*server* using Internet Explorer.</span></span> <span data-ttu-id="f7579-106">Si vous n'êtes pas en mesure de vous connecter de cette manière au serveur Web, ouvrez une invite de commandes et entrez la commande « NET START W3SVC ».</span><span class="sxs-lookup"><span data-stu-id="f7579-106">If you are unable to access the web server this way, go to a command prompt and enter the following command, "NET START W3SVC".</span></span>

2.  <span data-ttu-id="f7579-107">Dans le menu Démarrer, sélectionnez Exécuter.</span><span class="sxs-lookup"><span data-stu-id="f7579-107">From the Start menu, select Run.</span></span> <span data-ttu-id="f7579-108">Tapez msdfmap.ini et cliquez sur OK pour ouvrir le fichier msdfmap.ini dans le Bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="f7579-108">Type msdfmap.ini and click OK to open the msdfmap.ini file in Notepad.</span></span> <span data-ttu-id="f7579-109">Vérifier la \[CONNECT DEFAULT\] section et si le paramètre d’accès est défini sur NOACCESS, modifiez-la en READONLY.</span><span class="sxs-lookup"><span data-stu-id="f7579-109">Check the \[CONNECT DEFAULT\] section, and if the ACCESS parameter is set to NOACCESS, change it to READONLY.</span></span>

3.  <span data-ttu-id="f7579-110">À l’aide de l’utilitaire RegEdit, accédez à « HKEY\_LOCAL\_ordinateur\\logiciel\\Microsoft\\DataFactory\\HandlerInfo » et assurez-vous que **HandlerRequired** a la valeur 0 et **que DefaultHandler** correspond « » (Null chaîne).</span><span class="sxs-lookup"><span data-stu-id="f7579-110">Using the RegEdit utility, navigate to "HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\DataFactory\\HandlerInfo" and make sure **HandlerRequired** is set to 0 and **DefaultHandler** is "" (Null string).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="f7579-111">[!REMARQUE] Si vous modifiez cette section du Registre, vous devez redémarrer le service Publication World Wide Web en tapant les commandes « NET STOP W3SVC » puis « NET START W3SVC » à l'invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="f7579-111">If you make any changes to this section of the registry, you must stop and restart the World Wide Web Publishing Service by entering the following commands at a command prompt: "NET STOP W3SVC" and "NET START W3SVC".</span></span>

4.  <span data-ttu-id="f7579-112">À l’aide de l’utilitaire RegEdit, accédez à dans le registre » HKEY\_LOCAL\_ordinateur\\système\\CurrentControlSet\\Services\\W3SVC\\paramètres\\ADCLaunch » et vérifiez qu’il existe une clé **appelé RDSServer.Datafactory**.</span><span class="sxs-lookup"><span data-stu-id="f7579-112">Using the RegEdit utility, navigate in the registry to "HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\W3SVC\\Parameters\\ADCLaunch" and verify that there is a key called **RDSServer.Datafactory**.</span></span> <span data-ttu-id="f7579-113">Dans le cas contraire, créez-la.</span><span class="sxs-lookup"><span data-stu-id="f7579-113">If not, create it.</span></span>

5.  <span data-ttu-id="f7579-114">À l’aide du Gestionnaire des Services Internet, accédez au site Web par défaut et afficher les propriétés de la racine virtuelle MSADC.</span><span class="sxs-lookup"><span data-stu-id="f7579-114">Using Internet Services Manager, go to the default website and view the properties of the MSADC virtual root.</span></span> <span data-ttu-id="f7579-115">Examinez l'onglet Sécurité de répertoire au niveau de la section « Restrictions par adresse IP et nom de domaine ».</span><span class="sxs-lookup"><span data-stu-id="f7579-115">Inspect the Directory Security/IP Address and Domain Name Restrictions.</span></span> <span data-ttu-id="f7579-116">Si la case à cocher « Accès refusé » est activée, sélectionnez « Accès autorisé ».</span><span class="sxs-lookup"><span data-stu-id="f7579-116">If the "Access is Denied" is checked then select "Granted".</span></span>

<span data-ttu-id="f7579-117">Essayez de redémarrer le serveur si ces modifications ne semblent pas résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="f7579-117">Be sure to try rebooting the server if the changes to do not appear to solve the problem at first.</span></span>

