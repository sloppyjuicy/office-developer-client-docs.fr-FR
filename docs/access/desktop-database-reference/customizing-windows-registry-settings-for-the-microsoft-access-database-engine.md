---
title: Personnalisation des paramètres du Registre Windows pour le moteur de base de données Microsoft Access
TOCTitle: Customizing Windows Registry Settings for the Microsoft Access Database Engine
ms:assetid: ca7e958a-ea26-d67d-45b9-10aeb1eac96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834346(v=office.15)
ms:contentKeyID: 48547690
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032168
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4a90981c936c933d2eadb191bbf0d2639cd8e641
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471687"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a><span data-ttu-id="ac0d7-102">Personnalisation des paramètres du registre Windows pour le moteur de base de données Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="ac0d7-102">Customizing Windows Registry Settings for the Microsoft Access Database Engine</span></span>


<span data-ttu-id="ac0d7-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ac0d7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ac0d7-p101">Si votre application ne fonctionne pas correctement avec la fonctionnalité par défaut du moteur de base de données Microsoft Access, vous devrez peut-être modifier les paramètres dans le registre Microsoft® Windows® en fonction de vos besoins. Le registre Windows peut aussi être utilisé pour ajuster le fonctionnement du pilote ISAM et ODBC pouvant être installé.</span><span class="sxs-lookup"><span data-stu-id="ac0d7-p101">If your application cannot work correctly with the default functionality of the Microsoft Access database engine, you may have to change the settings in the Microsoft® Windows® Registry to suit your needs. The Windows Registry can also be used to tune the operation of the installable ISAM and ODBC driver.</span></span>

<span data-ttu-id="ac0d7-106">Vous pouvez personnaliser les paramètres du registre Windows de quatre manières différentes :</span><span class="sxs-lookup"><span data-stu-id="ac0d7-106">You can customize the settings in the Windows Registry in four different ways:</span></span>

<span data-ttu-id="ac0d7-107">[Utilisation de Regedit.exe pour remplacer les paramètres par défaut](https://msdn.microsoft.com/library/ff193205\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="ac0d7-107">[Using Regedit.exe to Overwrite the Default Settings](https://msdn.microsoft.com/library/ff193205\(v=office.15\))</span></span>

<span data-ttu-id="ac0d7-108">[Création d'une portion dans l'arborescence du Registre de votre application pour gérer les paramètres](https://msdn.microsoft.com/library/ff836342\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="ac0d7-108">[Creating a Portion in Your Application's Registry Tree to Manage the Settings](https://msdn.microsoft.com/library/ff836342\(v=office.15\))</span></span>

<span data-ttu-id="ac0d7-109">[Utilisation de la méthode SetOption à partir de DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="ac0d7-109">[Using the SetOption Method from DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))</span></span>

<span data-ttu-id="ac0d7-110">[Utilisation des propriétés de connexion du Fournisseur OLE DB Microsoft pour Access](https://msdn.microsoft.com/library/ff196356\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="ac0d7-110">[Using the Connection Properties in the Microsoft OLE DB Provider for Access](https://msdn.microsoft.com/library/ff196356\(v=office.15\))</span></span>

