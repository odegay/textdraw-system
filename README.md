Example how to create an register:

```java
Panel panel = TextdrawSystem.createPanel(player);
		TextdrawSystem.setPanel(player, panel);

		panel.setDialogLayout(DialogLayout.FORM);
		panel.getLeftButton().setText(localizedStringSet.get(player, "Dialogs.Back"));
		panel.getRightButton().setText(localizedStringSet.get(player, "Dialogs.Next"));

//example panelDialog
PanelDialog panelDialog = TextdrawSystem.createPanelDialog(player);

		List list = panelDialog.addList("optionList");
		//create group
		list.addListItem("createGroup")
				.setClickHandler(handler -> createGroupDialog());

			//delete group
			list.addListItem("deleteGroup")
					.setClickHandler(handler -> deleteGroupDialog());

			//edit group
			list.addListItem("EditGroup")
					.setClickHandler(handler -> editGroupDialog());
		//edit player
		list.addListItem("EditPlayer")
				.setClickHandler(handler -> editPlayerOptionDialog());

		panelDialog.toggleOkButton(false);
		panelDialog.setCaption("Caption");

		panelDialog.show();
```