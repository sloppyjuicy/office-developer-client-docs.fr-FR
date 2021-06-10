---
title: Marquage d’objets métiers comme fiables pour l’écriture de scripts
TOCTitle: Marking business objects as safe for scripting
ms:assetid: 8ee49aec-672d-96f7-baa6-9261317a4d90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249630(v=office.15)
ms:contentKeyID: 48546295
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe5d331b7f3ab4685cb930323076d111a25ec68e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289776"
---
# <a name="marking-business-objects-as-safe-for-scripting"></a><span data-ttu-id="e5f44-102">Marquage d’objets métiers comme fiables pour l’écriture de scripts</span><span class="sxs-lookup"><span data-stu-id="e5f44-102">Marking business objects as safe for scripting</span></span>

<span data-ttu-id="e5f44-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e5f44-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e5f44-p101">Pour sécuriser un environnement Internet, vous devez marquer les objets métier instanciés avec la méthode [CreateObject](dataspace-object-rds.md) de l'objet [RDS.DataSpace](createobject-method-rds.md) comme étant « sûrs pour l'écriture de scripts ». Vous devez vérifier qu'ils sont reconnus en tant que tels dans la zone License du Registre système pour pouvoir les utiliser dans DCOM.</span><span class="sxs-lookup"><span data-stu-id="e5f44-p101">To help ensure a secure Internet environment, you need to mark any business objects instantiated with the [RDS.DataSpace](dataspace-object-rds.md) object's [CreateObject](createobject-method-rds.md) method as "safe for scripting." You need to ensure they are marked as such in the License area of the system registry before they can be used in DCOM.</span></span>

<span data-ttu-id="e5f44-p102">Pour configurer manuellement un objet métier reconnu sûr pour l'écriture de scripts, créez un fichier texte avec une extension .reg et placez-y le texte suivant. Les deux numéros suivants permettent d'activer la fonctionnalité de sécurité lors de l'écriture de scripts :</span><span class="sxs-lookup"><span data-stu-id="e5f44-p102">To manually mark your business object as safe for scripting, create a text file with a .reg extension that contains the following text. The following two numbers enable the safe-for-scripting feature:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95801-9882-11CF-9FA9-00AA006C42C4}] 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95802-9882-11CF-9FA9-00AA006C42C4}] 
```

<span data-ttu-id="e5f44-108">où \< *MyActiveXGUID* est le numéro \> GUID hexadécimal de votre objet métier.</span><span class="sxs-lookup"><span data-stu-id="e5f44-108">where \<*MyActiveXGUID*\> is the hexadecimal GUID number of your business object.</span></span> <span data-ttu-id="e5f44-109">Save it and merge it into your registry by using the Registry Editor or double-clicking the .reg file in Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="e5f44-109">Save it and merge it into your registry by using the Registry Editor or double-clicking the .reg file in Windows Explorer.</span></span>

<span data-ttu-id="e5f44-110">Les objets métier créés dans Microsoft Visual Basic peuvent être automatiquement marqués comme « sécurisés pour les scripts » à l’aide de l’Assistant Package et Déploiement.</span><span class="sxs-lookup"><span data-stu-id="e5f44-110">Business objects created in Microsoft Visual Basic can be automatically marked as "safe for scripting" with the Package and Deployment Wizard.</span></span> <span data-ttu-id="e5f44-111">Lorsque l'Assistant vous demande de spécifier les paramètres de sécurité, sélectionnez **Initialisation sécurisée** et **Scripts sécurisés**.</span><span class="sxs-lookup"><span data-stu-id="e5f44-111">When the wizard asks you to specify safety settings, select **Safe for initialization** and **Safe for scripting**.</span></span>

<span data-ttu-id="e5f44-p105">En dernier lieu, l'Assistant Configuration de l'application crée un fichier .htm et un fichier .cab. Vous pouvez copier ces deux fichiers sur l'ordinateur cible et double-cliquer sur le fichier .htm pour charger la page et enregistrer correctement le serveur.</span><span class="sxs-lookup"><span data-stu-id="e5f44-p105">On the last step, the Application Setup Wizard creates an .htm and a .cab file. You can then copy these two files to the target computer and double-click the .htm file to load the page and correctly register the server.</span></span>

<span data-ttu-id="e5f44-114">Étant donné que l’objet métier sera installé dans le répertoire Windows System32 Occache par défaut, déplacez-le dans le répertoire Windows System32 et modifiez la clé de Registre \\ \\ \\ **\_ HKEY CLASSES \_ ROOT \\ CLSID \\** \< *MyActiveXGUID* \> \\ **InprocServer32** pour qu’elle corresponde au chemin d’accès correct.</span><span class="sxs-lookup"><span data-stu-id="e5f44-114">Because the business object will be installed in the Windows\\System32\\Occache directory by default, move it to the Windows\\System32 directory and change the **HKEY\_CLASSES\_ROOT\\CLSID\\**\<*MyActiveXGUID*\>\\**InprocServer32** registry key to match the correct path.</span></span>


> [!NOTE]
> <span data-ttu-id="e5f44-p106">[!REMARQUE] Les objets métier reconnus sûrs pour l'écriture de scripts ou l'initialisation peuvent être instanciés et initialisés par n'importe qui sur le réseau. Les objets métier personnalisés ne doivent pas être conçus et implémentés à la légère. Il est impératif que ces objets ne représentent pas une menace de sécurité susceptible d'être exploitée par des pirates informatiques pour accéder à la zone sensible du serveur hôte et causer des dommages.</span><span class="sxs-lookup"><span data-stu-id="e5f44-p106">Business objects marked as safe for scripting or safe for initialization can be instantiated and initialized by anyone over the network. Any custom business object must not be designed and implemented casually. It is imperative that such objects do not present a security threat that hackers can explore to gain access to the sensitive area of the hosting server and inflict damages.</span></span>


