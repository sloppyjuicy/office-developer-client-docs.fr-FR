---
title: Personnalisation des paramètres du registre Windows pour le moteur de base de données Microsoft Access
TOCTitle: Customizing Windows registry settings for the Microsoft Access database engine
ms:assetid: ca7e958a-ea26-d67d-45b9-10aeb1eac96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834346(v=office.15)
ms:contentKeyID: 48547690
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032168
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7cbe8ad56e01249563f7b06c9018d923a96246e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295120"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a><span data-ttu-id="465e8-102">Personnalisation des paramètres du registre Windows pour le moteur de base de données Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="465e8-102">Customizing Windows registry settings for the Microsoft Access database engine</span></span>

<span data-ttu-id="465e8-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="465e8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="465e8-104">Si votre application ne fonctionne pas correctement avec les fonctionnalités par défaut du moteur de base de données Microsoft Access, vous de devez peut-être modifier les paramètres du Registre Microsoft Windows en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="465e8-104">If your application cannot work correctly with the default functionality of the Microsoft Access database engine, you may have to change the settings in the Microsoft Windows Registry to suit your needs.</span></span> <span data-ttu-id="465e8-105">Le registre Windows peut aussi être utilisé pour ajuster le fonctionnement du pilote ISAM et ODBC pouvant être installé.</span><span class="sxs-lookup"><span data-stu-id="465e8-105">The Windows Registry can also be used to tune the operation of the installable ISAM and ODBC driver.</span></span>

<span data-ttu-id="465e8-106">Vous pouvez personnaliser les paramètres du registre Windows de quatre manières différentes :</span><span class="sxs-lookup"><span data-stu-id="465e8-106">You can customize the settings in the Windows Registry in four different ways:</span></span>

- [<span data-ttu-id="465e8-107">Utilisation Regedit.exe pour réécrire les paramètres par défaut</span><span class="sxs-lookup"><span data-stu-id="465e8-107">Using Regedit.exe to overwrite the default settings</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-regedit-exe-to-overwrite-the-default-settings)
- [<span data-ttu-id="465e8-108">Création d’une partie dans l’arborescence du Registre de votre application pour gérer les paramètres</span><span class="sxs-lookup"><span data-stu-id="465e8-108">Creating a portion in your application's registry tree to manage the settings</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/creating-a-portion-in-your-application-s-registry-tree-to-manage-the-settings)
- [<span data-ttu-id="465e8-109">Utilisation de la méthode SetOption à partir de DAO</span><span class="sxs-lookup"><span data-stu-id="465e8-109">Using the SetOption method from DAO</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-setoption-method-from-dao)
- [<span data-ttu-id="465e8-110">Utilisation des propriétés Connection dans le fournisseur Microsoft OLE DB pour Access</span><span class="sxs-lookup"><span data-stu-id="465e8-110">Using the Connection properties in the Microsoft OLE DB Provider for Access</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-connection-properties-in-the-microsoft-ole-db-provider-for-access)

