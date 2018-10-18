---
title: Fournisseur OLE DB pour la publication Internet
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bf41e23b56a05c8c119713b7fb459a34ca526169
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602514"
---
# <a name="the-ole-db-provider-for-internet-publishing"></a>Fournisseur OLE DB pour la publication Internet


**S’applique à**: Access 2013 | Office 2013

<<<<<<< Les objets [Stream](stream-object-ado.md) ADO le chef [Record](record-object-ado.md) et utilisable avec le fournisseur Microsoft OLE DB pour la publication Internet (fournisseur de publication Internet) pour accéder aux ressources et les manipuler, tels que des dossiers Web ou fichiers pris en charge par Microsoft FrontPage. ADO permet de spécifier la source d'un objet **Record**, **Stream** ou [Recordset](recordset-object-ado.md) sous la forme d'une URL. Vous pouvez ensuite télécharger, déplacer, copier et supprimer les ressources ou manipuler directement leurs propriétés.
=== Les objets ADO [Record](record-object-ado.md) et [Stream](stream-object-ado.md) peuvent être utilisés avec le fournisseur Microsoft OLE DB pour la publication Internet (fournisseur de publication Internet) pour accéder et manipuler des ressources, telles que des dossiers web ou de fichiers pris en charge par Microsoft FrontPage. ADO permet de spécifier la source d'un objet **Record**, **Stream** ou [Recordset](recordset-object-ado.md) sous la forme d'une URL. Vous pouvez ensuite télécharger, déplacer, copier et supprimer les ressources ou manipuler directement leurs propriétés.
>>>>>>> master

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
> <P>Si Msdaipp.dso est explicitement spécifié comme valeur du fournisseur, avec le mot clé string de <EM>fournisseur de</EM> connexion ou de la propriété <STRONG>Provider</STRONG> , vous ne pouvez pas utiliser « URL = » dans la chaîne de connexion. Cela générerait une erreur. Au lieu de cela, spécifiez simplement l’URL comme indiqué ci-dessus.</P>



Pour plus d'informations sur le fournisseur de publication Internet, consultez [Fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md) ou la documentation du composant accompagnant l'application source avec laquelle le fournisseur OLE DB pour la publication Internet a été installé : Windows 2000, Office 2000 ou Internet Explorer 5.0.

