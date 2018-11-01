---
title: Fournisseur OLE DB pour la publication Internet
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3025637cf972f720db0a91b598d5903f13b8c9c4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886962"
---
# <a name="the-ole-db-provider-for-internet-publishing"></a><span data-ttu-id="6ecef-102">Fournisseur OLE DB pour la publication Internet</span><span class="sxs-lookup"><span data-stu-id="6ecef-102">The OLE DB Provider for Internet Publishing</span></span>


<span data-ttu-id="6ecef-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ecef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6ecef-104">Les objets ADO [Record](record-object-ado.md) et [Stream](stream-object-ado.md) peuvent être utilisés avec le fournisseur Microsoft OLE DB pour la publication Internet (fournisseur de publication Internet) pour accéder et manipuler des ressources, telles que des dossiers web ou de fichiers pris en charge par Microsoft FrontPage.</span><span class="sxs-lookup"><span data-stu-id="6ecef-104">The ADO [Record](record-object-ado.md) and [Stream](stream-object-ado.md) objects can be used with the Microsoft OLE DB Provider for Internet Publishing (Internet Publishing Provider) to access and manipulate resources, such as web folders or files served by Microsoft FrontPage.</span></span> <span data-ttu-id="6ecef-105">ADO permet de spécifier la source d'un objet **Record**, **Stream** ou [Recordset](recordset-object-ado.md) sous la forme d'une URL.</span><span class="sxs-lookup"><span data-stu-id="6ecef-105">With ADO, you can specify the source of a **Record**, **Stream**, or [Recordset](recordset-object-ado.md) to be a URL.</span></span> <span data-ttu-id="6ecef-106">Vous pouvez ensuite télécharger, déplacer, copier et supprimer les ressources ou manipuler directement leurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="6ecef-106">You can then upload, download, move, copy, and delete resources, or directly manipulate resource properties.</span></span>

<span data-ttu-id="6ecef-107">Pour consulter des exemples de code utilisant des objets **Record** et **Stream** avec le fournisseur de publication Internet, consultez [Scénario de publication Internet](internet-publishing-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="6ecef-107">For example code using **Records** and **Streams** with the Internet Publishing Provider, see the [Internet Publishing Scenario](internet-publishing-scenario.md).</span></span>

<span data-ttu-id="6ecef-p102">Le fournisseur de publication Internet est installé avec Microsoft Windows 2000. Des versions antérieures du fournisseur de publication Internet sont également disponibles avec Microsoft Office 2000 et Microsoft Internet Explorer 5.0.</span><span class="sxs-lookup"><span data-stu-id="6ecef-p102">The Internet Publishing Provider is installed with Microsoft Windows 2000. Earlier versions of the Internet Publishing Provider are also available with Microsoft Office 2000 and Microsoft Internet Explorer 5.0.</span></span>

<span data-ttu-id="6ecef-110">Il existe trois façons de connecter ADO au fournisseur de publication Internet :</span><span class="sxs-lookup"><span data-stu-id="6ecef-110">There are three ways to connect ADO to the Internet Publishing Provider:</span></span>

- <span data-ttu-id="6ecef-p103">Spécifiez « URL= » dans la chaîne de connexion. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="6ecef-p103">Specify "URL=" in the connection string. For example:</span></span>
    
  ```vb 
     
    objConn.Open "URL=https://servername" 
  ```

- <span data-ttu-id="6ecef-113">Spécifiez Msdaipp.dso pour le mot-clé *Provider* de la chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="6ecef-113">Specify Msdaipp.dso for the *Provider* keyword of the connection string.</span></span> <span data-ttu-id="6ecef-114">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="6ecef-114">For example:</span></span>
    
  ```vb 
     
    objConn.Open "provider=MSDAIPP.DSO;data source=https://servername" 
  ```

- <span data-ttu-id="6ecef-p105">Spécifiez Msdaipp.dso pour la propriété [Provider](provider-property-ado.md) de l'objet [Connection](connection-object-ado.md). Par exemple :</span><span class="sxs-lookup"><span data-stu-id="6ecef-p105">Specify Msdaipp.dso for the [Provider](provider-property-ado.md) property of the [Connection](connection-object-ado.md) object. For example:</span></span>
    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```


> [!NOTE]
> <P><span data-ttu-id="6ecef-117">Si Msdaipp.dso est explicitement spécifié comme valeur du fournisseur, avec le mot clé string de <EM>fournisseur de</EM> connexion ou de la propriété <STRONG>Provider</STRONG> , vous ne pouvez pas utiliser « URL = » dans la chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="6ecef-117">If Msdaipp.dso is explicitly specified as the value of the provider, either with the <EM>Provider</EM> connection string keyword or the <STRONG>Provider</STRONG> property, you cannot use "URL=" in the connection string.</span></span> <span data-ttu-id="6ecef-118">Cela générerait une erreur.</span><span class="sxs-lookup"><span data-stu-id="6ecef-118">If you do, an error will occur.</span></span> <span data-ttu-id="6ecef-119">Au lieu de cela, spécifiez simplement l’URL comme indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="6ecef-119">Instead, simply specify the URL as shown above.</span></span></P>



<span data-ttu-id="6ecef-120">Pour plus d'informations sur le fournisseur de publication Internet, consultez [Fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md) ou la documentation du composant accompagnant l'application source avec laquelle le fournisseur OLE DB pour la publication Internet a été installé : Windows 2000, Office 2000 ou Internet Explorer 5.0.</span><span class="sxs-lookup"><span data-stu-id="6ecef-120">For more specific information about the Internet Publishing Provider, see [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), or the provider documentation provided with the source application with which the OLE DB Provider for Internet Publishing was installed: Windows 2000, Office 2000, or Internet Explorer 5.0.</span></span>

