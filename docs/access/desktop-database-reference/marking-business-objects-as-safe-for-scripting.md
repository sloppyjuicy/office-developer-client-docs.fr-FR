---
title: Objets métier reconnus sûrs pour l'écriture de scripts
TOCTitle: Marking Business Objects as Safe for Scripting
ms:assetid: 8ee49aec-672d-96f7-baa6-9261317a4d90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249630(v=office.15)
ms:contentKeyID: 48546295
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7ac928f7e61cf633aac6963565cf3aae441a2ac6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471892"
---
# <a name="marking-business-objects-as-safe-for-scripting"></a>Objets métier reconnus sûrs pour l'écriture de scripts


**S’applique à**: Access 2013 | Office 2013

Pour sécuriser un environnement Internet, vous devez marquer les objets métier instanciés avec la méthode [CreateObject](dataspace-object-rds.md) de l'objet [RDS.DataSpace](createobject-method-rds.md) comme étant « sûrs pour l'écriture de scripts ». Vous devez vérifier qu'ils sont reconnus en tant que tels dans la zone License du Registre système pour pouvoir les utiliser dans DCOM.

Pour configurer manuellement un objet métier reconnu sûr pour l'écriture de scripts, créez un fichier texte avec une extension .reg et placez-y le texte suivant. Les deux numéros suivants permettent d'activer la fonctionnalité de sécurité lors de l'écriture de scripts :

```vb 
 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95801-9882-11CF-9FA9-00AA006C42C4}] 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95802-9882-11CF-9FA9-00AA006C42C4}] 
```

où \< *MyActiveXGUID* \> correspond au numéro GUID hexadécimal de votre objet métier. Enregistrer et fusionner dans votre Registre à l’aide de l’Éditeur du Registre ou en double-cliquant sur le fichier .reg dans l’Explorateur Windows.

Les objets métier créés dans Microsoft® Visual Basic peuvent être automatiquement marqués comme étant « sûrs pour l'écriture de scripts » par l'intermédiaire de l'Assistant Deployment Package Wizard. Lorsque l'Assistant vous demande de spécifier les paramètres de sécurité, sélectionnez **Initialisation sécurisée** et **Scripts sécurisés**.

En dernier lieu, l'Assistant Configuration de l'application crée un fichier .htm et un fichier .cab. Vous pouvez copier ces deux fichiers sur l'ordinateur cible et double-cliquer sur le fichier .htm pour charger la page et enregistrer correctement le serveur.

Étant donné que l’objet métier sera installé dans les fenêtres\\System32\\Occache répertoire par défaut, déplacez-le à Windows\\répertoire System32 et modifier la **HKEY\_CLASSES\_racine\\CLSID\\ ** \< *MyActiveXGUID*\>\\clé de Registre**InprocServer32** pour faire correspondre le chemin d’accès correct.


> [!NOTE]
> [!REMARQUE] Les objets métier reconnus sûrs pour l'écriture de scripts ou l'initialisation peuvent être instanciés et initialisés par n'importe qui sur le réseau. Les objets métier personnalisés ne doivent pas être conçus et implémentés à la légère. Il est impératif que ces objets ne représentent pas une menace de sécurité susceptible d'être exploitée par des pirates informatiques pour accéder à la zone sensible du serveur hôte et causer des dommages.


