---
<<<<<<< Titre tête : TOCTitle de la propriété ParentURL (ADO) : propriété ParentURL (ADO) === titre : ParentURL, propriété (ADO) TOCTitle : ParentURL, propriété (ADO)
>>>>>>> Master ms:assetid : ec7ec476-6f9e-8486-fe02-74995975df5c ms:mtpsurl : https://msdn.microsoft.com/library/JJ250200(v=office.15) ms:contentKeyID : ms.date 48548517 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="parenturl-property-ado"></a>ParentURL, propriété (ADO)
=======
# <a name="parenturl-property-ado"></a>ParentURL, propriété (ADO)
>>>>>>> master

**S’applique à**: Access 2013 | Office 2013

Indique la chaîne d'URL absolue qui pointe vers l'objet [Record](record-object-ado.md) parent de l'objet **Record** actif.

<<<<<<< Tête
## <a name="return-value"></a>Valeur renvoyée
=======
## <a name="return-value"></a>Valeur renvoyée
>>>>>>> master

Renvoie une valeur **String** qui indique l'URL de l'objet **Record** parent.

## <a name="remarks"></a>Remarques

La propriété **ParentURL** dépend de la source utilisée pour ouvrir l'objet **Record**. Cet objet **Record** peut par exemple être ouvert avec une source contenant le nom du chemin d'accès relatif à un répertoire référencé par la propriété [ActiveConnection](activeconnection-property-ado.md).

Supposons que « second » est un sous-dossier de « first ». Ouvrez l'objet **Record** comme indiqué ci-dessous :

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

À présent, la valeur de la propriété **ParentURL** est la propriété **ParentURL** devient «https://first», comme **ActiveConnection**.

La source peut également être une URL absolue, tel que «https://first/second». La propriété **ParentURL** devient alors «https://first», le niveau au-dessus. La propriété **ParentURL** devient alors «https://first», le niveau supérieur « seconde ».

La valeur de cette propriété peut être nulle si :

- L'objet actuel n'a pas de parent ; par exemple si l'objet **Record** est la racine d'un répertoire.

- L'objet **Record** représente une entité qui ne peut pas être spécifiée avec une URL.

Cette propriété est en lecture seule.


> [!NOTE]
> - [!REMARQUE] Cette propriété n'est prise en charge que par les fournisseurs sources des documents, comme le [Fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d'informations, voir [Enregistrements et champs spécifiques au fournisseur](records-and-provider-supplied-fields.md).
> - [!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le fournisseur Microsoft OLE DB pour la publication Internet. Pour plus d'informations, voir [URL relatives et absolues](absolute-and-relative-urls.md). 
> - [!REMARQUE] Si l'enregistrement actuel contient un enregistrement de données provenant d'un **Recordset** ADO, l'accès à la propriété **ParentURL** génère une erreur d'exécution, indiquant qu'aucune URL n'est possible.


