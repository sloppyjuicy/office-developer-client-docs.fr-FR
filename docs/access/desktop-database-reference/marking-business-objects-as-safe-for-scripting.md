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
# <a name="marking-business-objects-as-safe-for-scripting"></a>Marquage d’objets métiers comme fiables pour l’écriture de scripts

**S’applique à** : Access 2013, Office 2013

Pour sécuriser un environnement Internet, vous devez marquer les objets métier instanciés avec la méthode [CreateObject](dataspace-object-rds.md) de l'objet [RDS.DataSpace](createobject-method-rds.md) comme étant « sûrs pour l'écriture de scripts ». Vous devez vérifier qu'ils sont reconnus en tant que tels dans la zone License du Registre système pour pouvoir les utiliser dans DCOM.

Pour configurer manuellement un objet métier reconnu sûr pour l'écriture de scripts, créez un fichier texte avec une extension .reg et placez-y le texte suivant. Les deux numéros suivants permettent d'activer la fonctionnalité de sécurité lors de l'écriture de scripts :

```vb 
 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95801-9882-11CF-9FA9-00AA006C42C4}] 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95802-9882-11CF-9FA9-00AA006C42C4}] 
```

où \< *MyActiveXGUID* \> est le numéro de GUID hexadécimal de votre objet métier. Save it and merge it into your registry by using the Registry Editor or double-clicking the .reg file in Windows Explorer.

Les objets métier créés dans Microsoft Visual Basic peuvent être automatiquement marqués comme étant «sûrs pour l'écriture de scripts» dans l'Assistant emPaquetage et déploiement. Lorsque l'Assistant vous demande de spécifier les paramètres de sécurité, sélectionnez **Initialisation sécurisée** et **Scripts sécurisés**.

En dernier lieu, l'Assistant Configuration de l'application crée un fichier .htm et un fichier .cab. Vous pouvez copier ces deux fichiers sur l'ordinateur cible et double-cliquer sur le fichier .htm pour charger la page et enregistrer correctement le serveur.

Étant donné que l'objet métier est installé par défaut\\dans\\le répertoire Windows system32 occache, déplacez-le vers\\le répertoire Windows system32 et modifiez le **CLSID\\\\ racine de la classe\_\_HKEY** . \<Clé de Registre *MyActiveXGUID*\>\\**InprocServer32** correspondant au chemin d'accès correct.


> [!NOTE]
> [!REMARQUE] Les objets métier reconnus sûrs pour l'écriture de scripts ou l'initialisation peuvent être instanciés et initialisés par n'importe qui sur le réseau. Les objets métier personnalisés ne doivent pas être conçus et implémentés à la légère. Il est impératif que ces objets ne représentent pas une menace de sécurité susceptible d'être exploitée par des pirates informatiques pour accéder à la zone sensible du serveur hôte et causer des dommages.


