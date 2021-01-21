# react_ckeditor5_wiris

#CKEditor 5 editor generated with the online builder Including (wiris/MathType).

This Repository is developed by the ckeditor online builder.
--------------------------------------------------------------------------------

Rund Below command For the Integration

--------------------------------------------------------------------------------

npm i ckeditor5-custom-build-math-wiris

--------------------------------------------------------------------------------

Example to use this with react app.


import { CKEditor } from "@ckeditor/ckeditor5-react";
import ClassicEditor from 'ckeditor5-custom-build-math-wiris';

export default class YOURCLASS extends React.Component {
	render() {
		return(
			<CKEditor
				editor={ClassicEditor}
				data={"Content Goes Here.."}
				config={{
					toolbar: {
						items: [
							'heading', 
							'|',
							'MathType',
							'|',
							'bold',
							'italic',
							'|',
							'link',
							'bulletedList',
							'numberedList',
							'|',
							'imageUpload',
							'mediaEmbed',
							'|',
							'insertTable',
							'|',
							'blockQuote',
							'|',
							'undo',
							'redo'
						],
					},
					ckfinder: { uploadUrl: "Your Image Upload URL." },
				}}
				onReady={(editor) => {
				// You can store the "editor" and use when it is needed.
				console.log("Editor is ready to use!", editor);
				}}
				onChange={(event, editor) => {
				console.log("onChange.", editor);
				}}
				onBlur={(event, editor) => {
				console.log("Blur.", editor);
				}}
				onFocus={(event, editor) => {
				console.log("Focus.", editor);
				}}
				/>
		);
	}
}
