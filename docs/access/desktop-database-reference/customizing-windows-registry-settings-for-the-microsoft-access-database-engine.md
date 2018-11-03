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
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a>Personnalisation des paramètres du registre Windows pour le moteur de base de données Microsoft Access

**S’applique à**: Access 2013, Office 2013

Si votre application ne fonctionne pas correctement avec la fonctionnalité par défaut du moteur de base de données Microsoft Access, vous devrez modifier les paramètres dans le Registre Microsoft Windows pour répondre à vos besoins. Le registre Windows peut aussi être utilisé pour ajuster le fonctionnement du pilote ISAM et ODBC pouvant être installé.

Vous pouvez personnaliser les paramètres du registre Windows de quatre manières différentes :

- [Utilisation de Regedit.exe pour remplacer les paramètres par défaut](https://msdn.microsoft.com/library/ff193205\(v=office.15\))
- [Création d’une portion dans l’arborescence du Registre de votre application pour gérer les paramètres](https://msdn.microsoft.com/library/ff836342\(v=office.15\))
- [À l’aide de la méthode SetOption à partir de DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))
- [Utilisation des propriétés de connexion dans le fournisseur Microsoft OLE DB pour Access](https://msdn.microsoft.com/library/ff196356\(v=office.15\))

