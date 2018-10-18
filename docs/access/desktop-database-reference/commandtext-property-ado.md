---
<<<<<<< Titre tête : TOCTitle de propriété CommandText (ADO) : propriété CommandText (ADO) === titre : CommandText, propriété (ADO) TOCTitle : CommandText, propriété (ADO)
>>>>>>> Master ms:assetid : 0debec1c-068f-0aea-fce8-e61aa39c5907 ms:mtpsurl : https://msdn.microsoft.com/library/JJ248859(v=office.15) ms:contentKeyID : ms.date 48543234 : 18/09/2015 mtps_version : v=office.15 f1_keywords :
- Ado210.chm1231123 f1_categories :
- Office.Version=v15
---

<<<<<<< Tête
# <a name="commandtext-property-ado"></a>CommandText, propriété (ADO)
=======
# <a name="commandtext-property-ado"></a>CommandText, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique le texte d'une commande à émettre sur un fournisseur.

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une valeur de type **String** qui contient une commande de fournisseur, comme une instruction SQL, un nom de table, une URL relative ou un appel de procédure stockée. La valeur par défaut est "" (chaîne de longueur zéro).

## <a name="remarks"></a>Notes

Utilisez la propriété **CommandText** pour définir ou renvoyer le texte d'une commande représentée par un objet [Command](command-object-ado.md). En général, il s'agit d'une instruction SQL, mais il peut également s'agir d'un autre type d'instruction de commande reconnu par le fournisseur, comme un appel de procédure stockée. Le langage, ou la version, utilisé pour une instruction SQL doit être pris en charge par le processeur de requêtes du fournisseur.

<<<<<<< Tête si la propriété [Prepared](prepared-property-ado.md) de l’objet **Command** est définie sur **True** et l’objet **Command** est lié à une connexion ouverte lorsque vous définissez la propriété **CommandText** , ADO prépare la requête () Autrement dit, une forme compilée de la requête qui est stockée par le fournisseur) lorsque vous appelez les méthodes [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) ou **Open** .
=== Si la propriété [Prepared](prepared-property-ado.md) de l’objet **Command** est définie sur **True** et que l’objet **Command** est lié à une connexion ouverte lorsque vous définissez la propriété **CommandText** , ADO prépare la requête (c'est-à-dire, une forme compilée de la requête qui est stockée par le fournisseur) lorsque vous appelez les méthodes [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) ou **Open** .
>>>>>>> master

En fonction du paramètre de la propriété [CommandType](commandtype-property-ado.md), ADO peut modifier la propriété **CommandText**. Vous pouvez lire la propriété **CommandText** à tout moment pour découvrir le texte réel de la commande utilisé par ADO au cours de l'exécution.

Utilisez la propriété **CommandText** pour définir ou retourner une URL relative, spécifiant une ressource telle qu'un fichier ou un répertoire. La ressource est relative à un emplacement spécifié explicitement par une URL absolue ou spécifié implicitement par un objet [Connection](connection-object-ado.md) ouvert.


> [!NOTE]
<<<<<<< Tête
> <P>[!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le <A href="microsoft-ole-db-provider-for-internet-publishing.md">fournisseur Microsoft OLE DB pour la publication Internet</A>. Pour plus d'informations, consultez <A href="absolute-and-relative-urls.md">URL absolues et relatives</A>.</P>
=======
> [!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d’informations, consultez [URL absolues et relatives](absolute-and-relative-urls.md).
>>>>>>> master


