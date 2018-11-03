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
ms.openlocfilehash: 99e2b31cf686895a56e9d70b177314355c1aff3c
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945145"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a><span data-ttu-id="c60e8-102">Personnalisation des paramètres du registre Windows pour le moteur de base de données Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="c60e8-102">Customizing Windows registry settings for the Microsoft Access database engine</span></span>

<span data-ttu-id="c60e8-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c60e8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c60e8-104">Si votre application ne fonctionne pas correctement avec la fonctionnalité par défaut du moteur de base de données Microsoft Access, vous devrez modifier les paramètres dans le Registre Microsoft Windows pour répondre à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="c60e8-104">If your application cannot work correctly with the default functionality of the Microsoft Access database engine, you may have to change the settings in the Microsoft Windows Registry to suit your needs.</span></span> <span data-ttu-id="c60e8-105">Le registre Windows peut aussi être utilisé pour ajuster le fonctionnement du pilote ISAM et ODBC pouvant être installé.</span><span class="sxs-lookup"><span data-stu-id="c60e8-105">The Windows Registry can also be used to tune the operation of the installable ISAM and ODBC driver.</span></span>

<span data-ttu-id="c60e8-106">Vous pouvez personnaliser les paramètres du registre Windows de quatre manières différentes :</span><span class="sxs-lookup"><span data-stu-id="c60e8-106">You can customize the settings in the Windows Registry in four different ways:</span></span>

- <span data-ttu-id="c60e8-107">[Utilisation de Regedit.exe pour remplacer les paramètres par défaut](https://msdn.microsoft.com/library/ff193205\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="c60e8-107">[Using Regedit.exe to overwrite the default settings](https://msdn.microsoft.com/library/ff193205\(v=office.15\))</span></span>
- <span data-ttu-id="c60e8-108">[Création d’une portion dans l’arborescence du Registre de votre application pour gérer les paramètres](https://msdn.microsoft.com/library/ff836342\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="c60e8-108">[Creating a portion in your application's registry tree to manage the settings](https://msdn.microsoft.com/library/ff836342\(v=office.15\))</span></span>
- <span data-ttu-id="c60e8-109">[À l’aide de la méthode SetOption à partir de DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="c60e8-109">[Using the SetOption method from DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))</span></span>
- <span data-ttu-id="c60e8-110">[Utilisation des propriétés de connexion dans le fournisseur Microsoft OLE DB pour Access](https://msdn.microsoft.com/library/ff196356\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="c60e8-110">[Using the Connection properties in the Microsoft OLE DB Provider for Access](https://msdn.microsoft.com/library/ff196356\(v=office.15\))</span></span>

