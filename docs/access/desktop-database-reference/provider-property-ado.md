---
title: Provider, propriété (ADO)
TOCTitle: Provider Property (ADO)
ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15)
ms:contentKeyID: 48543543
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 890f80534ff47c4dea67b34f345bce0f90328c60
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469062"
---
# <a name="provider-property-ado"></a>Provider, propriété (ADO)


**S’applique à**: Access 2013 | Office 2013

Indique le nom du fournisseur d'un objet [Connection](connection-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs renvoyées

Définit ou renvoie une valeur **String** qui indique le nom du fournisseur.

## <a name="remarks"></a>Remarques

Utilisez la propriété **Provider** pour définir ou renvoyer le nom du fournisseur d’une connexion. Cette propriété peut aussi être définie par le contenu de la propriété [ConnectionString](connectionstring-property-ado.md) ou de l’argument *ConnectionString* de la méthode [Open](open-method-ado-connection.md). Toutefois, si l’on indique le fournisseur à plusieurs endroits et que l’on appelle la méthode **Open**, les résultats sont imprévisibles. Si aucun fournisseur n’est spécifié, la valeur par défaut de la propriété est MSDASQL ([Fournisseur Microsoft OLE DB pour ODBC](microsoft-ole-db-provider-for-odbc.md)).

La propriété **Provider** est en lecture/écriture lorsque la connexion est fermée et en lecture seule lorsqu'elle est ouverte. Le paramètre ne prend que lorsque l'on ouvre l'objet **Connection** ou que l'on accède à la collection [Properties](properties-collection-ado.md) de l'objet **Connection**. Si le paramètre n'est pas valide, une erreur est générée.

