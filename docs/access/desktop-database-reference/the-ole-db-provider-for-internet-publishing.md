---
title: Fournisseur OLE DB pour la publication Internet
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 617dca5ced5410e2023657ea1b0b748066f7843f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314055"
---
# <a name="ole-db-provider-for-internet-publishing"></a>Fournisseur OLE DB pour la publication Internet

**S’applique à** : Access 2013, Office 2013

Les objets Record et [Stream](stream-object-ado.md) [ADO](record-object-ado.md) peuvent être utilisés avec le fournisseur Microsoft OLE DB pour la publication Internet (fournisseur de publication Internet) pour accéder et manipuler des ressources, telles que des dossiers web ou des fichiers servis par Microsoft FrontPage. ADO permet de spécifier la source d'un objet **Record**, **Stream** ou [Recordset](recordset-object-ado.md) sous la forme d'une URL. Vous pouvez ensuite télécharger, déplacer, copier et supprimer les ressources ou manipuler directement leurs propriétés.

Pour consulter des exemples de code utilisant des objets **Record** et **Stream** avec le fournisseur de publication Internet, consultez [Scénario de publication Internet](internet-publishing-scenario.md).

Le fournisseur de publication Internet est installé avec Microsoft Windows 2000. Des versions antérieures du fournisseur de publication Internet sont également disponibles avec Microsoft Office 2000 et Microsoft Internet Explorer 5.0.

Il existe trois façons de connecter ADO au fournisseur de publication Internet :

- Spécifiez « URL= » dans la chaîne de connexion. Par exemple :
    
  ```vb 
     
    objConn.Open "URL=https://servername" 
  ```

- Spécifiez Msdaipp.dso pour le mot-clé *Provider* de la chaîne de connexion. Par exemple :
    
  ```vb 
     
    objConn.Open "provider=MSDAIPP.DSO;data source=https://servername" 
  ```

- Spécifiez Msdaipp.dso pour la propriété [Provider](provider-property-ado.md) de l'objet [Connection](connection-object-ado.md). Par exemple :
    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```

> [!NOTE]
> Si Msdaipp.dso est explicitement spécifié en tant que  valeur du fournisseur, avec le mot clé de chaîne de connexion Provider ou la propriété **Provider,** vous ne pouvez pas utiliser « URL= » dans la chaîne de connexion. Cela générerait une erreur. Spécifiez simplement l’URL comme indiqué précédemment dans cette rubrique.

Pour plus d'informations sur le fournisseur de publication Internet, consultez [Fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md) ou la documentation du composant accompagnant l'application source avec laquelle le fournisseur OLE DB pour la publication Internet a été installé : Windows 2000, Office 2000 ou Internet Explorer 5.0.

