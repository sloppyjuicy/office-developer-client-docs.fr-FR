---
<<<<<<< Titre tête : TOCTitle de la propriété ActiveConnection (ADO) : propriété ActiveConnection (ADO) ms:assetid : 5501b2d7-b62c-5fff-1edd-2b7efb3f8c4a ms:mtpsurl : https://msdn.microsoft.com/library/JJ249281(v=office.15) ms:contentKeyID : ms.date 48544918 : 18/09/2015 === titre : ActiveConnection, propriété (ADO) TOCTitle : ActiveConnection, propriété (ADO) ms:assetid : 5501b2d7-b62c-5fff-1edd-2b7efb3f8c4a ms:mtpsurl : https://msdn.microsoft.com/library/JJ249281(v=office.15) ms:contentKeyID : ms.date 48544918 : 17/10/2018
>>>>>>> maître mtps_version : v=office.15 f1_keywords :
- Ado210.chm1231115 f1_categories :
- Office.Version=v15
---

<<<<<<< Tête
# <a name="activeconnection-property-ado"></a>ActiveConnection, propriété (ADO)

=======
# <a name="activeconnection-property-ado"></a>ActiveConnection, propriété (ADO)
>>>>>>> master

**S’applique à**: Access 2013 | Office 2013

Indique l'objet [Connection](connection-object-ado.md) auquel l'objet [Command](command-object-ado.md), [Recordset](recordset-object-ado.md) ou [Record](record-object-ado.md) spécifié appartient actuellement.

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une valeur de type **String** contenant la définition d'une connexion si la connexion est fermée, ou une valeur **Variant** contenant l'objet **Connection** actif si la connexion est ouverte. La valeur par défaut est une référence d'objet Null. Reportez-vous à la propriété [ConnectionString](connectionstring-property-ado.md).

## <a name="remarks"></a>Notes

Utilisez la propriété **ActiveConnection** pour déterminer l'objet **Connection** sur lequel l'objet **Command** est exécuté ou sur lequel l'objet **Recordset** spécifié est ouvert.

<<<<<<< Tête **commande**

Pour les objets **Command**, la propriété **ActiveConnection** est en lecture/écriture.

Si vous tentez d'appeler la méthode [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) sur un objet **Command** avant d'affecter à cette propriété un objet **Connection** ouvert ou une chaîne de connexion valide, une erreur se produit.

<a name="microsoft-visual-basicsetting-the-activeconnection-property-to-nothing-disassociates-the-command-object-from-the-current-connection-and-causes-the-provider-to-release-any-associated-resources-on-the-data-source-you-can-then-associate-the-command-object-with-the-same-or-another-connection-object-some-providers-allow-you-to-change-the-property-setting-from-one-connection-to-another-without-having-to-first-set-the-property-to-nothing"></a>**Microsoft Visual Basic** Si la propriété **ActiveConnection** sur *Nothing* dissocie l’objet **Command** à partir de la **connexion** en cours et le fournisseur libérer les ressources associées dans la source de données. Vous pouvez alors associer l'objet **Command** au même objet **Connection** ou à un autre. Certains fournisseurs permettent de modifier le paramètre de propriété d’une **connexion** à un autre, sans devoir tout d’abord définir la propriété sur *Nothing*.
=======
### <a name="command"></a>Commande

Pour les objets **Command**, la propriété **ActiveConnection** est en lecture/écriture.

Si vous tentez d'appeler la méthode [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) sur un objet **Command** avant d'affecter à cette propriété un objet **Connection** ouvert ou une chaîne de connexion valide, une erreur se produit.

**Microsoft Visual Basic**: définition de la propriété **ActiveConnection** sur *Nothing* dissocie l’objet **Command** à partir de la **connexion** en cours et le fournisseur libérer les ressources associées dans les données source. Vous pouvez alors associer l'objet **Command** au même objet **Connection** ou à un autre. Certains fournisseurs permettent de modifier le paramètre de propriété d’une **connexion** à un autre, sans devoir tout d’abord définir la propriété sur *Nothing*.
>>>>>>> master

Si la collection [Parameters](parameters-collection-ado.md) de l’objet **Command** contient les paramètres fournis par le fournisseur, la collection est effacée si vous définissez la propriété **ActiveConnection** sur *Nothing* ou sur un autre objet **Connection** . Si vous créez des objets [Parameter](parameter-object-ado.md) et les utilisez pour remplir la collection **Parameters** de l’objet **Command** manuellement, paramètre **ActiveConnection** sur *Nothing* ou un autre objet **Connection** propriété quitte la collection **Parameters** intacte.

La fermeture de l'objet **Connection** auquel est associé un objet **Command** affecte à la propriété **ActiveConnection** la valeur *Nothing*. L'attribution d'un objet **Connection** fermé à cette propriété génère une erreur.

<<<<<<< Tête **jeu d’enregistrements**
=======
### <a name="recordset"></a>Recordset
>>>>>>> master

Pour les objets **Recordset** ouverts ou pour les objets **Recordset** dont la propriété [Source](source-property-ado-recordset.md) a pour valeur un objet **Command** valide, la propriété **ActiveConnection** est en lecture seule. Autrement, elle est en lecture/écriture.

Vous pouvez affecter à cette propriété un objet **Connection** valide ou une chaîne de connexion valide. Dans ce cas, le fournisseur crée un objet **Connection** à l'aide de cette définition et ouvre la connexion. De plus, le fournisseur peut définir cette propriété sur le nouvel objet **Connection** pour vous permettre d'accéder à l'objet **Connection** et obtenir des informations complémentaires relatives à l'objet ou exécuter d'autres commandes.

Si vous utilisez l’argument *ActiveConnection* de la méthode [Open](open-method-ado-recordset.md) pour ouvrir un objet **Recordset** , la propriété **ActiveConnection** héritera de la valeur de l’argument.

Si vous affectez à la propriété **Source** de l'objet **Recordset** une variable d'objet **Command** valide, la propriété **ActiveConnection** de l'objet **Recordset** hérite du paramètre de la propriété **ActiveConnection** de l'objet **Command**.

<<<<<<< Tête **L’utilisation à distance des services de données**lorsqu’elle est utilisée sur un objet Recordset côté client d’objet, cette propriété peut être définie qu’une chaîne de connexion ou (dans Microsoft Visual Basic ou Visual Basic, Scripting Edition) *Nothing*.

**Record**

Cette propriété est en lecture/écriture lorsque l'objet **Record** est fermé et peut contenir une chaîne de connexion ou une référence à un objet **Connection** ouvert. Cette propriété est en lecture seule lorsque l'objet **Record** est ouvert et qu'il contient une référence à un objet **Connection** ouvert.

Un objet **Connection** est créé implicitement lorsque l'objet **Record** est ouvert à partir d'une URL. Ouvrez l'objet **Record** à l'aide d'un objet **Connection** existant ouvert en affectant à cette propriété l'objet **Connection** ou en utilisant l'objet **Connection** comme paramètre dans l'appel de la méthode [Open](open-method-ado-record.md). Si l'objet **Record** est ouvert à partir d'un objet **Record** ou [Recordset](recordset-object-ado.md) existant, il est automatiquement associé à l'objet **Connection** de cet objet **Record** ou **Recordset**.


> [!NOTE]
> <P>[!REMARQUE] Les URL utilisant le schéma HTTP appellent automatiquement le <A href="microsoft-ole-db-provider-for-internet-publishing.md">fournisseur Microsoft OLE DB pour la publication Internet</A>. Pour plus d'informations, reportez-vous à la section <A href="absolute-and-relative-urls.md">URL absolues et relatives</A>.</P>
=======
**Utilisation de Service de données à distance**: lorsqu’elle est utilisée sur un objet Recordset de côté client, cette propriété peut être définie qu’une chaîne de connexion ou (dans Microsoft Visual Basic ou Visual Basic, Scripting Edition) *Nothing*.

### <a name="record"></a>Rappel

Cette propriété est en lecture/écriture lorsque l'objet **Record** est fermé et peut contenir une chaîne de connexion ou une référence à un objet **Connection** ouvert. Cette propriété est en lecture seule lorsque l'objet **Record** est ouvert et qu'il contient une référence à un objet **Connection** ouvert.

Un objet **Connection** est créé implicitement lorsque l'objet **Record** est ouvert à partir d'une URL. Ouvrez l'objet **Record** à l'aide d'un objet **Connection** existant ouvert en affectant à cette propriété l'objet **Connection** ou en utilisant l'objet **Connection** comme paramètre dans l'appel de la méthode [Open](open-method-ado-record.md). Si l' **enregistrement** est ouvert à partir d’un objet **Record** ou [Recordset](recordset-object-ado.md)existant, il est automatiquement associée à un objet de **connexion** de cet objet **Record** ou **Recordset** .

> [!NOTE]
> [!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d’informations, consultez [URL absolues et relatives](absolute-and-relative-urls.md).

>>>>>>> master


