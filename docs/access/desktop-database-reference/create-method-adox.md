---
title: Create, méthode (ADOX)
TOCTitle: Create Method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 91f5105611df85e007dea6d0e17e3104ea5987a3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870253"
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

