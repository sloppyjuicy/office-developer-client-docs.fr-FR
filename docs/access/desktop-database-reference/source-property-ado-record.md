---
title: Source, propriété (objet Record ADO)
TOCTitle: Source Property (ADO Record)
ms:assetid: f36f0f5f-4493-d8c5-db4b-c72f5031bcb3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250235(v=office.15)
ms:contentKeyID: 48548670
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d6e010ce8db93baaf8faddaeff5ab4dabda6a84
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603384"
---
# <a name="source-property-ado-record"></a>Source, propriété (objet Record ADO)


**S’applique à**: Access 2013 | Office 2013

Indique la source de données ou l'objet que représente l'objet [Record](record-object-ado.md).

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une valeur **Variant** qui indique l'entité que représente l'objet **Record**.

## <a name="remarks"></a>Remarques

La propriété **Source** renvoie l’argument *Source* de la méthode [Open](open-method-ado-record.md) de l’objet **Record** . Elle peut contenir une chaîne représentant une URL absolue ou relative. Une URL absolue peut être utilisée sans que la propriété [ActiveConnection](activeconnection-property-ado.md) ne soit définie pour ouvrir directement l'objet **Record**. Dans ce cas, un objet **Connection** implicite est créé.

La propriété **Source** peut également contenir une référence à un **Recordset** déjà ouvert, ce qui ouvre un objet **Record** représentant la ligne actuelle dans le **Recordset**.

La propriété **Source** peut également contenir une référence à un objet [Command](command-object-ado.md) qui renvoie du fournisseur une seule ligne de données.

Si la propriété **ActiveConnection** est elle aussi définie, la propriété **Source** doit pointer vers un objet à la portée de cette connexion. Par exemple, dans les espaces de noms structurés en arborescence, si la propriété **Source** contient une URL absolue, elle doit par exemple pointer vers un nœud à la portée du nœud identifié par l'URL dans la chaîne de connexion. Si la propriété **Source** contient une URL relative, cette URL est validée dans le contexte défini par la propriété **ActiveConnection**.

La propriété **Source** est accessible en lecture/écriture lorsque l'objet **Record** est fermé et en lecture seule lorsque l'objet **Record** est ouvert.

<<<<<<< Tête

> [!NOTE]
> <P>[!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le <A href="microsoft-ole-db-provider-for-internet-publishing.md">fournisseur Microsoft OLE DB pour la publication Internet</A>. Pour plus d'informations, consultez <A href="absolute-and-relative-urls.md">URL absolues et relatives</A>.</P>
=======
> [!NOTE]
> [!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d’informations, consultez [URL absolues et relatives](absolute-and-relative-urls.md).
>>>>>>> master


