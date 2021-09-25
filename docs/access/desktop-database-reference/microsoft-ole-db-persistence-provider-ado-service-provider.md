---
title: Fournisseur de persistance Microsoft OLE DB (fournisseur de service ADO)
TOCTitle: Microsoft OLE DB Persistence Provider (ADO Service Provider)
ms:assetid: 22e41769-36eb-5a88-05ed-870938657624
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249007(v=office.15)
ms:contentKeyID: 48543719
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7b021daeb4d43be52d0b8c8409e3be866b8b27b2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589364"
---
# <a name="microsoft-ole-db-persistence-provider-ado-service-provider"></a>Fournisseur de persistance Microsoft OLE DB (fournisseur de services ADO)


**S’applique à** : Access 2013, Office 2013 

The Microsoft OLE DB Persistence Provider enables you to save a [Recordset](recordset-object-ado.md) object into a file, and later restore that **Recordset** object from the file. Schema information, data, and pending changes are preserved.

Vous pouvez enregistrer le **Recordset** au format ADTG (Advanced Data Table Gram) ou au format XML ouvert (Extensible Markup Language).

## <a name="provider-keyword"></a>Mot clé du fournisseur

Pour appeler ce fournisseur, spécifiez le mot clé et la valeur suivants dans la chaîne de connexion.

```vb 
 
"Provider=MSPersist" 
```

## <a name="errors"></a>Erreurs

Les erreurs suivantes émises par ce fournisseur peuvent être détectées dans votre application.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>E_BADSTREAM</p></td>
<td><p>Le fichier ouvert n'a pas un format valide (c'est-à-dire que son format n'est ni ADTG, ni XML ).</p></td>
</tr>
<tr class="even">
<td><p>E_CANTPERSISTROWSET</p></td>
<td><p>L'objet <strong>Recordset</strong> enregistré présente des caractéristiques qui l'empêchent d'être stocké.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Le fournisseur de persistance Microsoft OLE DB n’expose pas de propriétés dynamiques.

Actuellement, seuls les objets **Recordset** hiérarchiques paramétrés ne peuvent pas être enregistrés.

Pour plus d’informations sur le stockage persistant des objets **Recordset**, consultez la rubrique [Informations complémentaires sur la persistance des objets Recordset](more-about-recordset-persistence.md).

Lorsqu'un flux est utilisé pour ouvrir un **Recordset**, seul le paramètre *Source* de la méthode **Open** doit être spécifié.

