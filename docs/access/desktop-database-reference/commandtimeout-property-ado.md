---
<<<<<<< Titre tête : TOCTitle de la propriété CommandTimeout (ADO) : propriété CommandTimeout (ADO) === titre : CommandTimeout, propriété (ADO) TOCTitle : CommandTimeout, propriété (ADO)
>>>>>>> Master ms:assetid : a0b6209c-9feb-08ae-002a-15d1d20734a8 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249739(v=office.15) ms:contentKeyID : ms.date 48546714 : 18/09/2015 mtps_version : v=office.15 f1_keywords :
- Ado210.chm1231124 f1_categories :
- Office.Version=v15
---

<<<<<<< Tête
# <a name="commandtimeout-property-ado"></a>CommandTimeout, propriété (ADO)
=======
# <a name="commandtimeout-property-ado"></a>CommandTimeout, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique le délai d'attente pour l'exécution d'une commande avant l'abandon de la tentative et la génération d'une erreur.

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une valeur de type **Long** indiquant, en secondes, le délai d'attente pour l'exécution d'une commande. La valeur par défaut est 30.

## <a name="remarks"></a>Notes

<<<<<<< Tête d’utiliser la propriété **CommandTimeout** sur un objet [Connection](connection-object-ado.md) ou un objet [Command](command-object-ado.md) pour permettre l’annulation d’un appel de méthode [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) , en raison de délais réseau trafic ou intensive d’utilisation de serveur. Si l'intervalle défini dans la propriété **CommandTimeout** s'écoule avant que la commande ait fini de s'exécuter, une erreur se produit et ADO annule la commande. Si vous attribuez la valeur 0 à la propriété, ADO attend indéfiniment que l'exécution se termine. Assurez-vous que le fournisseur et la source de données dans lesquels vous écrivez le code prennent en charge la fonctionnalité **CommandTimeout**.
=== D’utiliser la propriété **CommandTimeout** sur un objet [Connection](connection-object-ado.md) ou un objet [Command](command-object-ado.md) pour permettre l’annulation d’un appel de la méthode [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) , en raison de délais réseau trafic ou intensive d’utilisation de serveur. Si l'intervalle défini dans la propriété **CommandTimeout** s'écoule avant que la commande ait fini de s'exécuter, une erreur se produit et ADO annule la commande. Si vous attribuez la valeur 0 à la propriété, ADO attend indéfiniment que l'exécution se termine. Assurez-vous que le fournisseur et la source de données dans lesquels vous écrivez le code prennent en charge la fonctionnalité **CommandTimeout**.
>>>>>>> master

Le paramètre de **CommandTimeout** d'un objet **Connection** n'a aucun effet sur le paramètre de **CommandTimeout** d'un objet **Command** sur le même objet **Connection**. En d'autres termes, la propriété **CommandTimeout** de l'objet **Command** n'hérite pas de la valeur de la propriété **CommandTimeout** de l'objet **Connection**.

Sur un objet **Connection** , la propriété **CommandTimeout** reste en lecture/écriture après l’ouverture de la **connexion** .

