---
title: Méthode Stat - ActiveX Data Objects (ADO)
TOCTitle: Stat Method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6bc4ff8076ec07d065ba932ef0e0017edb97e703
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606954"
---
# <a name="stat-method-ado"></a>Stat, méthode (ADO)


**S’applique à**: Access 2013 | Office 2013

Extrait des informations relatives à un objet **Stream**.

## <a name="syntax"></a>Syntaxe

Longueur du *flux*. Stat (*StatStg*, *StatFlag*)

<<<<<<< Tête
## <a name="return-value"></a>Valeur renvoyée
=======
## <a name="return-value"></a>Valeur renvoyée
>>>>>>> master

Valeur de type Long indiquant l'état de l'opération.

## <a name="parameters"></a>Paramètres

  - *StatStg*

  - Structure STATSTG contenant des informations relatives au flux. L'implémentation de la méthode Stat utilisée par l'objet Stream ADO ne remplit pas tous les champs de la structure.

  - *StatFlag*

  - Indique que cette méthode ne renvoie pas certains membres dans la structure STATSTG, ce qui permet d'éviter une opération d'allocation de mémoire. Les valeurs sont extraites de l'énumération STATFLAG.  
      
    L'énumération STATFLAG possède deux valeurs.
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p>Constant</p></th>
    <th><p>Valeur</p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>STATFLAG_DEFAULT</p></td>
    <td><p>0</p></td>
    </tr>
    <tr class="even">
    <td><p>STATFLAG_NONAME</p></td>
    <td><p>1</p></td>
    </tr>
    </tbody>
    </table>


## <a name="remarks"></a>Notes

La version de la méthode Stat implémentée pour l'objet Stream ADO remplit les champs de la structure STATSTG suivants :

  - *pwcsName*

  - Une chaîne contenant le nom du flux, si elle est disponible et le StatFlag valeur STATFLAG\_anonyme n’a pas été spécifié.

  - *cbSize*

  - Indique la taille en octets du flux ou du tableau d'octets.

  - *mtime*

  - Indique l'heure de dernière modification de ce stockage, flux ou tableau d'octets.

  - *ctime*

  - Indique l'heure de création de ce stockage, flux ou tableau d'octets.

  - *atime*

  - Indique l'heure du dernier accès à ce stockage, flux ou tableau d'octets.

Si STATFLAG\_anonyme est spécifié dans le paramètre StatFlag, le nom du flux n’est pas retourné.

Si STATFLAG\_anonyme n’a pas été spécifié dans le paramètre StatFlag et aucun nom n’est disponible pour le flux actif, cette valeur sera E\_NOTIMPL.

