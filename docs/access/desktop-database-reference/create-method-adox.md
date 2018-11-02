---
title: Create, méthode (ADOX)
TOCTitle: Create method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 01f45adaf5bdd15841be86bfea62cca58e21a9d9
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925513"
---
# <a name="create-method-adox"></a>Create, méthode (ADOX)


**S’applique à**: Access 2013, Office 2013


Crée un catalogue.

## <a name="syntax"></a>Syntaxe

*Catalogue*. Créer*ConnectString*

## <a name="parameters"></a>Paramètres

  - *ConnectString*

  - Valeur de type **String** utilisée pour se connecter à la source de données.

## <a name="remarks"></a>Notes

La méthode **Create** crée et ouvre un nouvel objet ADO [Connection](connection-object-ado.md) à la source de données spécifiée dans le paramètre *ConnectString*. En cas de réussite, le nouvel objet **Connection** est affecté à la propriété [ActiveConnection](activeconnection-property-adox.md).

Une erreur se produit si le fournisseur ne prend pas en charge la création de catalogues.

