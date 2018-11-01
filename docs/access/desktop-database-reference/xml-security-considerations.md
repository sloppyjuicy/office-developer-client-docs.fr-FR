---
title: Notes sur la sécurité XML
TOCTitle: XML Security Considerations
ms:assetid: ef2c7f59-f5a2-98d1-37c6-42cb35b26a40
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250214(v=office.15)
ms:contentKeyID: 48548575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 69672b2993cb91ace5bd447b762f33fcbd66c1bc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868489"
---
# <a name="xml-security-considerations"></a><span data-ttu-id="c61e6-102">Notes sur la sécurité XML</span><span class="sxs-lookup"><span data-stu-id="c61e6-102">XML Security Considerations</span></span>


<span data-ttu-id="c61e6-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c61e6-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="xml-security-considerations"></a><span data-ttu-id="c61e6-104">Considérations relatives à la sécurité XML</span><span class="sxs-lookup"><span data-stu-id="c61e6-104">XML Security Considerations</span></span>

<span data-ttu-id="c61e6-p101">Les méthodes ADO **Record** et **Open** de l'objet **Recordset** ne peuvent être considérées comme des opérations sûres avec Internet Explorer. Si ces méthodes sont utilisées dans un code de script s'exécutant dans une application ou un contrôle sur un navigateur hôte, la configuration de sécurité du navigateur aura une influence sur son fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="c61e6-p101">The ADO **Save** and **Open** methods on the **Recordset** object are not considered safe operations to run in Internet Explorer. Thus, if these methods are used in a script code that is running in an application or control that is hosted in a browser, the security configuration of the browser will have an effect on its behavior.</span></span>

<span data-ttu-id="c61e6-p102">Internet Explorer 5 dispose de restrictions de sécurité pour ce type d'opérations par défaut dans les zones Internet. Avec cette configuration, l'objet **Recordset** ne peut pas accéder au système de fichiers local sur le client, ni accéder aux sources de données en dehors du domaine du serveur à partir duquel la page a été téléchargée. Plus précisément, lorsqu'il est exécuté sur un navigateur hôte, un objet **Recordset** ne peut être à nouveau enregistré dans un fichier que s'il se trouve sur le même serveur à partir duquel la page a été téléchargée. De la même façon, vous pouvez ouvrir un objet **Recordset** en le chargeant à partir d'un fichier uniquement si ce dernier réside sur le même serveur à partir duquel la page a été téléchargée.</span><span class="sxs-lookup"><span data-stu-id="c61e6-p102">Internet Explorer 5 provides security restrictions for such operations by default in the Internet zones. Under that configuration, the **Recordset** cannot make any access to the local file system on the client or access any data sources outside the domain of the server from which the page has been downloaded. Specifically, when running inside the browser host, a **Recordset** can be saved back to a file only if it is on the same server from which the page was downloaded. Similarly, you can open a **Recordset** by loading it from a file only if that file is on the same server from which the page was downloaded.</span></span>

<span data-ttu-id="c61e6-111">Pour plus d'informations sur la sécurité avec Internet Explorer, consultez l'article technique "Problèmes de sécurité ADO et RDS dans Microsoft Internet Explorer."</span><span class="sxs-lookup"><span data-stu-id="c61e6-111">For more information about security in Internet Explorer, see the technical article "ADO and RDS Security Issues in Microsoft Internet Explorer."</span></span>

