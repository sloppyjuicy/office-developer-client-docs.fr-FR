---
title: GetPermissions, méthode (ADOX)
TOCTitle: GetPermissions Method (ADOX)
ms:assetid: 98a2b2b6-a8af-15ee-b052-622a6f0661b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249683(v=office.15)
ms:contentKeyID: 48546496
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 388cbc5a69f57778d8a9a46db8d1dbec5ddf09d6
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604961"
---
# <a name="getpermissions-method-adox"></a>GetPermissions, méthode (ADOX)


**S’applique à**: Access 2013 | Office 2013


Renvoie les autorisations d'un groupe ou d'un utilisateur sur un objet ou un conteneur d'objets.

## <a name="syntax"></a>Syntaxe

*Valeur False* = *Groupe_ou_utilisateur*. GetPermissions (*nom*, *ObjectType* \[,*ObjectTypeId*\])

<<<<<<< Tête
## <a name="return-value"></a>Valeur renvoyée
=======
## <a name="return-value"></a>Valeur renvoyée
>>>>>>> master

Renvoie une valeur de type **Long** qui spécifie un masque de bits contenant les autorisations que le groupe ou l'utilisateur ont sur l'objet. Cette valeur peut correspondre à une ou plusieurs constantes [RightsEnum](rightsenum.md).

## <a name="parameters"></a>Paramètres

  - *Name*

  - Valeur de type **Variant** qui spécifie le nom de l'objet dont il faut définir les autorisations. Définir le *nom* à une valeur null si vous souhaitez obtenir des autorisations pour le conteneur d’objet.

  - *ObjectType*

  - Valeur de type **Long** qui peut être l'une des constantes [ObjectTypeEnum](objecttypeenum.md), spécifiant le type d'objet dont il faut obtenir les autorisations.

  - *ObjectTypeId*

  - Facultatif. Une valeur de **type Variant** qui spécifie le GUID pour un type d’objet fournisseur non défini par la spécification OLE DB. Ce paramètre est requis si *ObjectType* a la valeur **adPermObjProviderSpecific**. dans le cas contraire, il n’est pas utilisé.

