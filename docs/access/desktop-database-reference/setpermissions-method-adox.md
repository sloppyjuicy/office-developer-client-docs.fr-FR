---
title: SetPermissions, méthode (ADOX)
TOCTitle: SetPermissions method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d99608a938598135d713375875da9073c8f9f3c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927514"
---
# <a name="setpermissions-method-adox"></a>SetPermissions, méthode (ADOX)


**S’applique à**: Access 2013, Office 2013



Spécifie les autorisations d'un groupe ou d'un utilisateur sur un objet.

## <a name="syntax"></a>Syntaxe

*Groupe_ou_utilisateur*. SetPermissions*nom*, *ObjectType*, *Action*, *droits* \[,*hériter* \] \[,*ObjectTypeId*\]

## <a name="parameters"></a>Paramètres

  - *Name*

  - Valeur de type **String** qui spécifie le nom de l'objet dont il faut définir les autorisations.

  - *ObjectType*

  - Valeur de type **Long** qui peut être l'une des constantes [ObjectTypeEnum](objecttypeenum.md), spécifiant le type d'objet dont il faut obtenir les autorisations.

  - *Action*

  - Valeur de type **Long** qui peut correspondre à l'une des constantes [ActionEnum](actionenum.md), spécifiant le type d'action à effectuer lors de la configuration des autorisations.

  - *Rights*

  - Valeur de type **Long** qui peut être un masque de bits d'une ou plusieurs constantes [RightsEnum](rightsenum.md), indiquant les droits à définir.

  - *Inherit*

  - Facultatif. Valeur de type **Long** qui peut correspondre à l'une des constantes [InheritTypeEnum](inherittypeenum.md), qui spécifie la manière dont les objets héritent des autorisations. La valeur par défaut est **adInheritNone**.

  - *ObjectTypeId*

  - Facultatif. Une valeur de **type Variant** qui spécifie le GUID pour un type d’objet fournisseur non défini par la spécification OLE DB. Ce paramètre est requis si *ObjectType* a la valeur **adPermObjProviderSpecific**. dans le cas contraire, il n’est pas utilisé.

## <a name="remarks"></a>Notes

Une erreur se produit si le fournisseur ne prend pas en charge la définition de droits d'accès pour les groupes ou utilisateurs.


> [!NOTE]
> <P>Lorsque vous appelez la <STRONG>méthode SetPermissions</STRONG>, la définition des Actions à <STRONG>adAccessRevoke</STRONG> remplace tous les paramètres du paramètre <EM>droits</EM> . Ne définissez pas les <EM>Actions</EM> à <STRONG>adAccessRevoke</STRONG> si vous souhaitez que les droits spécifiés dans le paramètre <EM>Rights</EM> prenne effet.</P>


