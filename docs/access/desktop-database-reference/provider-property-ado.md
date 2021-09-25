---
title: Provider, propriété (ADO)
TOCTitle: Provider property (ADO)
ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15)
ms:contentKeyID: 48543543
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e63ec7813a1bc446502900de75369c9c42afd709
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565078"
---
# <a name="provider-property-ado"></a>Provider, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique le nom du fournisseur d'un objet [Connection](connection-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur **String** qui indique le nom du fournisseur.

## <a name="remarks"></a>Remarques

Utilisez la propriété **Provider** pour définir ou renvoyer le nom du fournisseur d’une connexion. Cette propriété peut aussi être définie par le contenu de la propriété [ConnectionString](connectionstring-property-ado.md) ou de l’argument *ConnectionString* de la méthode [Open](open-method-ado-connection.md). Toutefois, si l’on indique le fournisseur à plusieurs endroits et que l’on appelle la méthode **Open**, les résultats sont imprévisibles. Si aucun fournisseur n’est spécifié, la valeur par défaut de la propriété est MSDASQL ([Fournisseur Microsoft OLE DB pour ODBC](microsoft-ole-db-provider-for-odbc.md)).

La propriété **Provider** est en lecture/écriture lorsque la connexion est fermée et en lecture seule lorsqu’elle est ouverte. Le paramètre ne prend que lorsque l’on ouvre l’objet **Connection** ou que l’on accède à la collection [Properties](properties-collection-ado.md) de l’objet **Connection**. Si le paramètre n’est pas valide, une erreur est générée.

