---
<<<<<<< Titre tête : TOCTitle de la propriété CacheSize (ADO) : propriété CacheSize (ADO) === titre : CacheSize, propriété (ADO) TOCTitle : CacheSize, propriété (ADO)
>>>>>>> Master ms:assetid : 42f86cc0-30dc-669b-9e65-5e7ecd52c4d7 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249200(v=office.15) ms:contentKeyID : ms.date 48544491 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="cachesize-property-ado"></a>CacheSize, propriété (ADO)
=======
# <a name="cachesize-property-ado"></a>CacheSize, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique le nombre d'enregistrements dans un objet [Recordset](recordset-object-ado.md), placés dans la mémoire cache locale.

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une valeur de type **Long** qui doit être supérieure à 0. La valeur par défaut est 1.

## <a name="remarks"></a>Notes

Utilisez la propriété **CacheSize** pour contrôler le nombre d'enregistrements à récupérer simultanément à partir du fournisseur pour les insérer dans la mémoire locale. Par exemple, si **CacheSize** a pour valeur 10, après la première ouverture de l'objet **Recordset**, le fournisseur extrait les dix premiers enregistrements pour les insérer dans la mémoire locale. À mesure que vous parcourez l'objet **Recordset**, le fournisseur retourne les données du tampon de mémoire local. Dès que vous avez dépassé le dernier enregistrement du cache, le fournisseur récupère les dix enregistrements suivants de la source de données pour les insérer dans le cache.


> [!NOTE]
> <P>[!REMARQUE] <STRONG>CacheSize</STRONG> est basé sur la propriété spécifique au fournisseur, <STRONG>Maximum Open Rows</STRONG>, (dans la collection <STRONG>Properties</STRONG> de l'objet <STRONG>Recordset</STRONG> ). Vous ne pouvez pas affecter à <STRONG>CacheSize</STRONG> une valeur supérieure à celle de la propriété <STRONG>Maximum Open Rows</STRONG>. Pour modifier le nombre de lignes que le fournisseur peut ouvrir, définissez <STRONG>Maximum Open Rows</STRONG>.</P>



La valeur de **CacheSize** peut être ajustée au cours de la durée de vie de l'objet **Recordset**, mais si vous modifiez cette valeur, cela n'affecte que le nombre d'enregistrements présents en mémoire cache après plusieurs extractions successives de la source de données. La seule modification de la valeur de la propriété ne modifie pas le contenu actuel du cache.

S'il y a moins d'enregistrements à récupérer que ne l'indique la propriété **CacheSize**, le fournisseur renvoie les enregistrements restants et aucune erreur n'est générée.

Vous ne pouvez pas utiliser un paramètre **CacheSize** de valeur zéro. Dans ce cas, une erreur est générée.

Les enregistrements extraits du cache ne reflètent pas les modifications simultanées apportées aux données sources par d'autres utilisateurs. Pour forcer la mise à jour de toutes les données mises en cache, utilisez la méthode [Resync](resync-method-ado.md).

Si **CacheSize** a une valeur supérieure à 1, les méthodes de navigation ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext et MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) peuvent parfois accéder à un enregistrement supprimé, si une suppression a lieu après l’extraction des enregistrements. Après l’extraction initiale, les suppressions suivantes ne sont pas reflétées dans le cache de données tant que vous ne tentez pas d’accéder à une valeur de donnée d’une ligne supprimée. Cependant, si vous attribuez la valeur 1 à **CacheSize**, le problème ne se pose pas puisque les lignes supprimées ne peuvent pas être extraites.

